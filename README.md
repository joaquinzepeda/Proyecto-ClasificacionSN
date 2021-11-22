![banner](bin/cropped-logo-fcfm-die-1.png)  
# Proyecto de clasificación supervisada de SuperNovas para el curso EL4106  
Integrantes : Joaquin Zepeda, Benjamin Irarrazabal  
Tutor : Pablo Montero   
## Descripción del proyecto
En este proyecto se busca clasificar, de forma supervisada, series de tiempo astronómicas de supernovas. Estas series en astronomía son conocidas como curvas de luz, las cuáles entregan información sobre el brillo estelar, su error y el día en que ocurrió. Dicha información será extraída de la base de datos provista por el equipo del Automatic Learning for the Rapid Classification of Events (ALeRCE) el cuál es un broker de alertas astronómicas que recibe y procesa observaciones provenientes del survey astronómico Zwicky Transient Facility (ZTF). La base de datos está compuesta por cerca de 2000 curvas de luz de supernovas (correspondientes a SNIa, SNIbc, SNII, SNIIb, SNIIn, SNSL) y posee un alto desbalance entre la cantidad de curvas de luz de cada clase.
 
Ustedes deberán inspeccionar, visualizar y preprocesar los datos para luego extraer características de cada curva de luz. Una vez teniendo las características deberán trabajarlas y proponer un modelo supervisado que permita clasificarlas según su determinada clase. Para cumplir con lo anterior, propongan una estrategia para entrenar y evaluar el desempeño bajo un contexto de desbalance. Finalmente deberán estudiar la relevancia que tiene cada característica en la clasificación final. 
Con respecto a las variantes, deberán estudiar 3 algoritmos de clasificación donde al menos 1 debe ser distinto al del otro grupo. El algoritmo que escojan deberá ser estudiado a cabalidad, además deberán investigar e implementar técnicas de proyección/reducción de dimensionalidad de los vectores de características y lidiar con el desbalance de las clases . 






**Instrucciones para ejecutar el código:**  
1.	Para la **extracción de características** se debe ejecutar el archivo SN_feature_extraction.ipynb  
  1.1.	Si se ejecuta utilizando jupyter notebook es necesario tener instaladas las librerías de Alerce, esto puede ser complicado si es que no se trabaja en un ambiente de Linux.  
  1.2.	Si se ejecuta utilizando Google Colab, se debe ejecutar el “Bloque inicial”, luego reiniciar el entorno de ejecución (Reiniciar el kernel) para luego ejecutar los bloques.              
  
         `!python -m pip install Cython      
          !python -m pip install -e git+https://git@github.com/alercebroker/turbo-fats#egg=turbofats  
          !python -m pip install -e git+https://git@github.com/alercebroker/mhps#egg=mhps  
          !python -m pip install -e git+https://git@github.com/alercebroker/P4J#egg=P4J   
          !python -m pip install pyarrow  
          !python -m pip install -e git+https://git@github.com/alercebroker/lc_classifier#egg=lc_classifier`

2.	Para la **clasificación de supernovas utilizando Random Forest** se debe ejecutar el archivo Clasificación de Supernovas RF.ipynb.   
    2.1.1.	 No se recomienda ejecutar los bloques de “Random Forest Hyperparameter tuning” pues estos toman mucho tiempo, pero es posible observar los resultados.
3.	Para la **clasificación de supernovas utilizando una red MLP** se debe ejecutar el archivo Clasificación de Supernovas MLP.ipynb.   
  
