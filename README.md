# Reconocimiento de imagenes para Hackaton Innosoft
## Aplicación de redes neuronales convolucionales a el reconocimiento de enfermedades pulmonares en imagenes clinicas

### Resultados

Los resultados para este problema han sido variados en función de los hiperparametros usados. Para concretar, todos los resultados han sidos llevados a cabo usando la tecnica de data augmentation, la cual favorece a la fase de entrenamiento del modelo diversificando la cantidad de imagenes con las que entrena.

En principio, comenzando con un learning rate de 1e4 y unos 3 epochs, hayaba una gran cantidad de overfitting, pasando de un resultado de 60% de precision en el modelo a un 20% en test.Además, con un tamaño objetivo de la imagen (el tamaño que se le pasaria a la red neuronal) de 900x1200 encontraba grandes problemas de memoria, por lo que se dividio ese tamaño a la mitad. 

Despues, se probo que con un solo epoch, aunque daba unos resultados esperanzadores (50% de precisión en test), podia ser mejorable, pero no con un epoch entero. Por ello, dado qu se habian preestablecido 100 batches para entrenar, se decidió empezar a hacer un unico entrenamiento con 100 batches y un segundo entrenamiento con 50. Esto mejoró increiblemente los resultados pasando a una precision del 66% en entrenamiento y una precisión del 77% en test
