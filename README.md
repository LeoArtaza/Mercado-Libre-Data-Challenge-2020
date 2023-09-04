# Mercado Libre Data Challenge 2020

En esta competencia se debía predecir qué item un usuario compraría en base a su historial de navegación. Se podían adivinar 10 items, en orden, y también se ganaba puntos por adivinar la categoría.

Dado que la mitad de los datos de navegación eran búsquedas de texto, comencé construyendo un modelo en base a la tabla de items (x = nombre de item, y = categoría) que prediga qué categoría se buscaba.

![image](https://github.com/LeoArtaza/Mercado-Libre-Data-Challenge-2020/assets/57342159/c3c7832b-8731-4694-82f7-6a10aad46902)

Como se ve en estos ejemplos, la precisión era bastante buena (precisión de 69%)

![image](https://github.com/LeoArtaza/Mercado-Libre-Data-Challenge-2020/assets/57342159/e2b7a001-a30b-4b7b-9732-9033ef621156)

Luego construí otro modelo que, en base a las categorías buscadas o visitadas, adivinara las 10 categorías más probables de haberse comprado. Acá se ve cómo mejora la predicción con el modelo, vs. un baseline hecho a partir de adivinar los ítems vistos en orden inverso.

![image](https://github.com/LeoArtaza/Mercado-Libre-Data-Challenge-2020/assets/57342159/fb3d4a80-e9a9-47a1-bffa-1df2e55c4365)

Por último, adivinaba que el ítem que se había comprado era uno que se había visto, pero esta vez dentro de la categoría con mayor probabilidad según el modelo.

En retrospectiva, podría haber hecho un modelo de tipo clustering que adivine ítems similares para los otros 9 ítems predichos, dado que, en el modelo actual, si el usuario visitó 1 solo ítem, el resto de los ítems adivinados, eran los más vendidos de las categorías predichas, lo cual era una suposición bastante débil.
