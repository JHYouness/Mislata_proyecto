
epochs=300
redes_capas=[[3],[4,3],[4,8,3],[4,8,16,8,3],[4,8,16,32,16,8,4,3],[4,8,16,32,64,32,16,8,4,3],[4,8,16,32,64,128,64,32,16,8,4,3]]
activations=[
        ("Sigmoid","sigmoid"),
        ("Tan Hiperbolica","tanh"),
        ("ReLU","relu"),
        ("Leaky ReLU",tf.keras.layers.LeakyReLU()),
        ("ELU","elu"),
        ("SeLU","selu")]

figure=plt.figure(figsize=(9*len(activations), 9*len(redes_capas))) 

index=1
for capas in redes_capas:
  for caption,activation in activations:

    history,model=compile_fit(capas,activation,"sigmoid","categorical_crossentropy",epochs,x_train, x_test, y_train, y_test)
    axes = figure.add_subplot(len(redes_capas),len(activations),index)
    plot_metrics(axes,history.history,caption+ " " + str(capas))


    index=index+1

figure.tight_layout()

