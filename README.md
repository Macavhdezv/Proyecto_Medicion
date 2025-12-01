#### Proyecto Medición

# Análisis del Nivel Educacional y Resultados Electorales en los Plebiscitos Constitucionales 2022-2023 (Chile)
<img width="1280" height="490" alt="image" src="https://github.com/user-attachments/assets/fc561337-0058-4c13-ac3e-605064a9c1c7" />

### Introducción
El proyecto busca analizar la relación entre el nivel educacional promedio de las comunas chilenas y los resultados electorales obtenidos en los plebiscitos constitucionales de salida de 2022 y 2023, ambos realizados bajo voto obligatorio.

El objetivo es observar cómo factores socioeducativos influyen en la orientación del voto en procesos políticos de alta relevancia.

### Pregunta de investigación

¿Cómo se relaciona el nivel educacional de las comunas en Chile con el resultado positivo de los Plebiscitos de Salida de los procesos constituyentes 2022 y 2023?

### Marco Teórico
El proyecto analiza cómo las variables socioeconómicas, especialmente la educación, influyen en el comportamiento electoral en Chile.
Investigaciones clásicas ya destacaban que la educación es uno de los principales factores que explican la participación política. En América Latina, también se ha observado que el lugar de residencia y el nivel de ingresos afectan el voto: las zonas urbanas suelen participar menos, y dentro de ellas, los sectores más acomodados votan más que los de menores ingresos.

En Chile, la reforma electoral de 2012 marcó un fuerte descenso en la participación, con un promedio cercano al 48% en elecciones presidenciales posteriores. Esta caída acentuó el sesgo de clase en el voto, especialmente en distritos urbanos.

Los plebiscitos constitucionales de 2022 y 2023, ambos con voto obligatorio, ofrecen una oportunidad para observar cambios en este comportamiento. Estos procesos movilizaron a nuevos votantes —particularmente personas con menor nivel educacional—, permitiendo comparar cómo un electorado similar reaccionó de manera distinta en dos eventos consecutivos.

### Bases de datos y variables

## Variable Independiente:
1. Resultados-Plebiscito-Constitucional-2022.xlsx: Base de datos del Servel que nos envió la profe --> Variables que tomamos: comuna, opcion y votos_tricel (cantidad de votos x opción)
2. 2023_PlebiscitoConstitucional_DatosPlebiscito.xlsx: Base de datos del Servel que nos envió la profe --> Variables que tomamos: comuna, opcion y votos_tricel (cantidad de votos x opción)

## Variables de Control:
1. P7_Educacion_2.xlsx: Base de datos de CASEN --> Variable que obtuvimos: Niveles de educación x comuna
2. P7_Educacion_4.xlsx: Base de datos de CASEN --> Variable que obtuvimos: Niveles de educación x comuna y sexo
3. D1_Poblacion-censada-por-sexo-y-edad-en-grupos-quinquenales.xlsx: Base de datos del CENSO 2024 --> Variable que obtuvimos: Grupos de edad unidos --> categorizamos en 20-34, 35-49, 50-64. 65-79 y 80+, cada una con N° (1, 2, 3, 4, 5)
4. datos_alcalde.xlsx: Base de datos del SERVEL del 2022 --> Variable que obtuvimos: Tendencia política de la comuna (a partir de la coalición del alcalde)
5. Estimaciones_Tasa_Pobreza_Ingresos_Comunas_2022.xlsx: Base de datos de INE --> Variable que obtuvimos: nivel de pobreza x comuna.

Sacamos la variable de "Zona" porque habían categorías con muy pocos casos, haciendo que la estimación sea inestable.

Tampoco consideramos en el análisis a la Antártica porque no tenían datos de muchas de nuestras variables. 

El trabajo con las bases de datos se nos dio de forma muy fácil, solo que al ser tantas, tuvimos que hacer muchas modificaciones para que estén todas iguales. Por ejemplo, tuvimos que cambiarle el nombre de las comunas a casi todas las bases de datos para que conincidieran. También, hubieron bases de datos donde, al momento de limpiarlas, se unificaron variables.  

### Gráficos
A continuación, se presenta una descripción de los gráficos exploratorios en función a nuestras variables.

*Gráfico 1: Escolaridad promedio de mujeres y apoyo a Apruebo 2022*

<img width="450" height="300" alt="1escolaridadprom_mujeres_apruebo" src="https://github.com/user-attachments/assets/dfaba6d1-90a6-4b5a-9759-bd5b5a3f1b7a" />

Se presenta una tendencia positiva, en la cual las comunas con mayor escolaridad promedio de mujeres tienden a mostrar un mayor porcentaje de votos por el Apruebo. Además, se observa una dispersión moderada, por lo que la escolaridad influye significativamente, pero no explica por sí sola la totalidad del resultado. En relación a los Outliers, existe una escolaridad promedio femenina muy alta, pero se presenta un apoyo al Apruebo extremadamente bajo.

*Gráfico 2: Escolaridad promedio de hombres y apoyo a Apruebo 2022*

<img width="450" height="300" alt="2escolaridadprom_hombres_apruebo" src="https://github.com/user-attachments/assets/69ffdcf3-a47a-4727-88a5-d695b14e714b" />

Se presenta una tendencia positiva clara, en la cual las comunas con mayor escolaridad promedio de hombres tienden a mostrar un mayor porcentaje de votos por el Apruebo. Además, se observa una dispersión moderada, por lo que el nivel de escolaridad influye, pero no explica por sí solo el resultado. En relación a los Outliers, existe una escolaridad promedio extremadamente alta, pero se presenta un apoyo al Apruebo muy bajo.

*Gráfico 3: Escolaridad promedio de mujeres y apoyo al A favor 2023*

<img width="450" height="300" alt="3escolaridadprom_mujeres_Afavor" src="https://github.com/user-attachments/assets/a536dd2a-b8c0-4ae5-a801-53bc379293ca" />

se presenta una tendencia negativa, en la cual las comunas con mayor escolaridad promedio de mujeres tienden a mostrar un menor porcentaje de votos por la opción A favor. Además, se observa una dispersión moderada, por lo que la escolaridad influye, pero no explica por sí sola el resultado. En relación a los Outliers, existe una escolaridad promedio femenina extremadamente alta, pero se presenta un apoyo al A favor.

*Gráfico 4: Escolaridad promedio de hombres y apoyo al A favor 2023*

<img width="450" height="300" alt="4escolaridadprom_hombres_afavor" src="https://github.com/user-attachments/assets/aa19f6f7-0684-45e2-8874-446de0c80c8c" />

Se presenta una tendencia negativa leve, en la cual las comunas con mayor promedio de años de escolaridad de hombres tienden a mostrar un menor porcentaje de apoyo a la opción "A favor". Además, se observa una dispersión considerable, por lo que la escolaridad influye, pero no explica por sí sola el resultado electoral. En relación a los Outliers, existe una muy alta escolaridad promedio, pero a diferencia de la tendencia general, se presenta un apoyo extremadamente alto a la opción "A favor".

*Gráfico 5: Porcentaje de pobreza comunal y apoyo al Apruebo 2022*

<img width="450" height="300" alt="5pobreza_apruebo" src="https://github.com/user-attachments/assets/94da9f5c-08c8-4a4e-abef-5e1810369135" />

Se presenta una tendencia negativa, en la cual las comunas con mayor porcentaje de pobreza tienden a mostrar un menor porcentaje de votos por el Apruebo. Además, se observa una dispersión moderada, por lo que el nivel de pobreza influye, pero no explica por sí solo el resultado. En relación a los Outliers, existe un porcentaje de pobreza casi nulo, pero se presenta un apoyo al Apruebo extremadamente bajo, rompiendo con el inicio de la línea de tendencia que sugería un apoyo mayor en sectores de menor pobreza.

*Gráfico 6: Porcentaje de pobreza comunal y apoyo al A favor 2023*

<img width="450" height="300" alt="6pobreza_afavor" src="https://github.com/user-attachments/assets/26c15be0-5b0d-420f-843b-b496cf77ac4f" />

Se presenta una tendencia positiva, en la cual las comunas con mayor porcentaje de pobreza tienden a mostrar un mayor porcentaje de votos por la opción A favor. Además, se observa una dispersión moderada, por lo que el nivel de pobreza influye, pero no explica totalmente el resultado. En relación a los Outliers, existe un porcentaje de pobreza mínimo, pero se presenta un apoyo al "A favor" excepcionalmente alto, comportándose de manera opuesta a lo que la tendencia general predice para los sectores de baja pobreza.

*Gráfico 7: Porcentaje de mujeres comunal y apoyo A favor 2023*

<img width="450" height="300" alt="7mujerescomunal_Afavor" src="https://github.com/user-attachments/assets/77f06f47-d6eb-49f4-a338-fe147164693c" />

Se presenta una tendencia levemente positiva, en la cual las comunas con mayor porcentaje de mujeres en su población tienden a mostrar un aumento en el porcentaje de votos por el A favor.  Además, se observa una alta dispersión, concentrada mayoritariamente en el centro del gráfico, por lo que la proporción demográfica de mujeres influye mínimamente y no explica por sí sola el resultado. En relación a los Outliers, ambos presentan un apoyo al A favor extremadamente alto, escapando significativamente de la media, independientemente de que su porcentaje de mujeres sea cercano al promedio.

*Gráfico 8: Porcentaje de hombres comunal y apoyo A favor 2023*

<img width="450" height="300" alt="8hombrescomunal_afavor" src="https://github.com/user-attachments/assets/cd739f4b-4937-4d64-824e-32dff651f580" />

Se presenta una tendencia negativa muy leve, en la cual las comunas con mayor porcentaje de hombres tienden a mostrar una ligera disminución en el porcentaje de votos por el A favor. Además, se observa una alta concentración y dispersión de los datos en el centro, por lo que la composición demográfica por sexo influye mínimamente en el resultado. En relación a los Outliers, ambos presentan un apoyo al A favor extremadamente alto, escapando de la nube de dispersión principal, independientemente de su porcentaje de población masculina.

*Gráfico 9: Porcentaje de mujeres comunal y apoyo al Apruebo 2022*

<img width="450" height="300" alt="9mujerescom_apruebo" src="https://github.com/user-attachments/assets/d68dde8f-646a-481a-a452-20f58cd883fa" />

Se presenta una tendencia levemente negativa, en la cual las comunas con mayor porcentaje de mujeres en su población tienden a mostrar una ligera disminución en el porcentaje de votos por el Apruebo. Además, se observa una alta concentración y dispersión, por lo que la variable demográfica tiene muy poca capacidad explicativa sobre el resultado electoral. En relación a los Outliers, que se ubica muy por debajo de la nube de puntos principal, presentando un apoyo al Apruebo extremadamente bajo, independientemente de su composición de género.

*Gráfico 10: Porcentaje de hombres comunal y apoyo al Apruebo 2022*

<img width="450" height="300" alt="10hombrecom_apruebo" src="https://github.com/user-attachments/assets/06e94562-eb0a-463f-9b1b-69d426756aac" />

Se presenta una tendencia levemente positiva, en la cual las comunas con mayor porcentaje de hombres en su población tienden a mostrar un ligero aumento en el porcentaje de votos por el Apruebo. Además, se observa una alta concentración y dispersión de los datos, lo que sugiere que la proporción de hombres no es un factor determinante para explicar la variabilidad del resultado. En relación a los Outliers, a pesar de tener una proporción de hombres cercana al promedio, presenta un apoyo al Apruebo extremadamente bajo, situándose muy por debajo de la tendencia general.

*Gráfico 11: Distribución del apoyo al Apruebo 2022*

<img width="450" height="300" alt="11tendencia_alcalde_apruebo" src="https://github.com/user-attachments/assets/4d9ac98a-ea59-463d-8cfc-8bc8ace25a88" />

Se presenta una correlación, en la cual las comunas con alcaldes de Derecha tienden a concentrarse masivamente en un apoyo “Muy Bajo” al Apruebo, mientras que aquellas con alcaldes de Izquierda muestran una tendencia inversa, inclinándose hacia un apoyo “Alto”. Además, en el segmento de Independientes se observa una distribución homogénea (plana), por lo que la administración independiente no define una tendencia clara de voto. 
Por otra parte, los extremos, destaca la fuerte polarización, ya que 51 municipios de derecha se ubicaron en el nivel de apoyo más bajo, contrastando fuertemente con los municipios de izquierda, que mayoritariamente se ubicaron en el cuartil de apoyo más alto.

*Gráfico 12: Distribución del apoyo al A favor 2023*

<img width="450" height="300" alt="12tendencia_alcalde_afavor" src="https://github.com/user-attachments/assets/817945bc-a6dc-4d3b-94e8-9b13942e0c78" />

Se presenta una fuerte correlación política, en la cual las comunas con alcaldes de Derecha muestran una tendencia claramente ascendente, concentrándose masivamente en un apoyo “Alto” a la opción “A favor”. Por el contrario, los municipios con alcaldes de Izquierda e Independientes presentan una tendencia inversa, inclinándose mayoritariamente hacia un apoyo “Muy Bajo”. Además, se observa que el sector Independiente se alinea más con el comportamiento de la izquierda en este proceso. 

Por otra parte, los extremos, destaca la gran brecha en el cuartil de apoyo "Alto", mientras la derecha ubica a 56 de sus municipios, la izquierda solo cuenta con 12 en ese nivel de respaldo.

*Gráfico 13: Votación del Apruebo y educación superior por comuna*

<img width="450" height="300" alt="13edu_superior_apruebo" src="https://github.com/user-attachments/assets/3322d418-dc93-49a6-92da-bf048aaae476" />

Se presenta una tendencia positiva clara, en la cual las comunas con mayor porcentaje de población con educación superior tienden a mostrar un mayor porcentaje de votos por el Apruebo. Además, se observa una dispersión moderada en el tramo medio, lo que sugiere una correlación importante entre el nivel educativo profesional y la preferencia por esta opción. En relación a los Outliers, existe un porcentaje de educación superior excepcionalmente alto, pero se presenta un apoyo al Apruebo extremadamente bajo, rompiendo drásticamente con la proyección de la línea de tendencia.

*Gráfico 14: Votación del A favor y educación superior por comuna*

<img width="450" height="300" alt="14edu_superior_afavor" src="https://github.com/user-attachments/assets/c9766072-fcb9-4e2c-9126-5a8d552d4c4a" />

Se presenta una tendencia negativa leve, en la cual las comunas con mayor porcentaje de población con educación superior tienden a mostrar una disminución en el porcentaje de votos por la opción A favor. Además, se observa una dispersión considerable en los tramos medios, por lo que el nivel educativo influye parcialmente, pero no explica por sí solo el resultado. En relación a los Outliers, existe un porcentaje de educación superior extremadamente alto, pero se presenta un apoyo al A favor muy elevado, rompiendo completamente con la tendencia decreciente que rige para el resto de las comunas.

*Gráfico 15: Distribución del apoyo al Apruebo 2022 con Rango Etario*

<img width="450" height="300" alt="18rango_etario_apruebo" src="https://github.com/user-attachments/assets/42d2bb57-e515-42b6-a44a-d40037e24c59" />

Se presenta una marcada brecha generacional, en la cual los municipios asociados al rango etario joven (20-34 años) tienden a concentrarse mayoritariamente en un apoyo "Alto" al Apruebo. Por el contrario, el segmento de mayor edad (50-64 años) muestra una tendencia inversa, inclinándose masivamente hacia un apoyo "Muy Bajo". Además, el grupo intermedio (35-49 años) presenta una distribución más dispersa y centrada en los niveles medios, actuando como una transición entre ambos polos demográficos. En relación a los extremos, el grupo joven posiciona a 60 municipios en el cuartil de mayor apoyo, el grupo de 50-64 años ubica a 59 municipios en el nivel de apoyo más bajo.

*Gráfico 16: Distribución del apoyo A Favor 2023 con Rango Etario*

<img width="450" height="300" alt="19rango_etario_afavor" src="https://github.com/user-attachments/assets/2d213b62-1243-4a2d-8699-debbf81172a3" />

Se presenta una tendencia generacional inversa a la del proceso 2022, en la cual las comunas con población joven (20-34 años) tienden a concentrarse masivamente en un apoyo "Muy Bajo" a la opción "A favor". Por el contrario, el segmento de mayor edad (50-64 años) muestra una tendencia ascendente, inclinándose mayoritariamente hacia un apoyo "Alto". Además, el grupo intermedio (35-49 años) mantiene una participación más baja y dispersa sin una inclinación tan determinante. En relación a los extremos, hay 56 municipios jóvenes rechazaron la propuesta (nivel Muy Bajo), mientras que 59 municipios de mayor edad la apoyaron fuertemente (nivel Alto).

*Mapa 1: Educación Superior*
Porcentaje de personas con educación superior por comuna 

<img width="857" height="947" alt="15RM_edu_superior" src="https://github.com/user-attachments/assets/11f21012-3bc8-4f38-9b1c-d1906cb8a480" />

El mapa presenta una marcada concentración en el sector oriente, donde se observan las comunas con los niveles más altos en porcentajes de personas con educación superior, mientras que las zonas centrales y del sur presentan valores intermedios. En contraste, las comunas periféricas y con mayor carácter rural exhiben los porcentajes más bajos. Este patrón refleja las desigualdades territoriales tradicionales de la región, donde el acceso y la culminación de estudios superiores se asocian fuertemente con las diferencias socioeconómicas entre comunas.

*Mapa 2:  Mapa a Favor en plebiscito de 2023*

<img width="811" height="944" alt="16RM_apruebo" src="https://github.com/user-attachments/assets/cab60d70-8412-4fa2-aee3-952169bb4a28" />

El mapa presenta que el apoyo al “A favor” en el plebiscito de 2023 se concentró principalmente en comunas del sector oriente de la Región Metropolitana, donde los tonos más oscuros indican porcentajes más altos de voto favorable. En contraste, la mayor parte del territorio regional presenta valores intermedios o bajos, especialmente en comunas periféricas y del sur y poniente, donde el apoyo fue considerablemente menor. En conjunto, la distribución refleja una fuerte segmentación territorial del voto, con mayor adhesión en zonas de mayor nivel socioeconómico y menor respaldo en áreas urbanas populares y rurales.

*Mapa 3: Mapa apoyo al Apruebo en el plebiscito de 2022*

<img width="811" height="950" alt="17RM_afavor" src="https://github.com/user-attachments/assets/3d376e57-dc5d-44f5-ae56-9a20ec3e7b4d" />

El mapa presenta que el apoyo al Apruebo en el plebiscito de 2022 se concentró especialmente en comunas del centro y sur de la Región Metropolitana, donde predominan los tonos más oscuros, mientras que las comunas del sector oriente exhibieron los porcentajes más bajos de respaldo, reflejados en colores más claros; esta distribución evidencia un patrón territorial en el que las zonas populares y periféricas manifestaron mayor apoyo al Apruebo, en contraste con las comunas de mayores ingresos, donde la opción obtuvo menor votación.

## Modelos de Regresión:

Se utilizaron modelos de Regresión Lineal Múltiple y Regresión Logística, controlando por variables de pobreza, género, edad y tendencia política.

Los resultados de los modelos se resumen en las siguientes tablas:

<img width="532" height="855" alt="image" src="https://github.com/user-attachments/assets/a35d5b7a-3ee4-4cf8-8e4a-0cd72658d577" />

<img width="535" height="824" alt="image" src="https://github.com/user-attachments/assets/bb022d28-f382-4bc7-91d7-328e20a24f4a" />

## Respuesta a nuestra pregunta de investigación:

La relación entre educación y el voto en este caso no es lineal ni constante, sino que sufrió una inversión estructural entre ambos procesos:
1. En el Plebiscito de Salida del 2022 la escolaridad femenina actuó como un soporte del "Apruebo", mientras que el resto de la élite profesional tendió al rechazo.
2. En el Plebsicito de Salida del 2023 se generó una "Coalición de Extremos". El "A Favor" representado por el conservadurismo, ganó en la élite profesional y en sectores vulnerables, pero fue rechazado por la clase media con alto promedio de escolaridad.

## Análisis de los modelos:

Al ver los coeficientes de los modelos, se observa que la educación opera en dos dimensiones distitntas que parecen contrapuestas, por una parte, la educación de élite (% con educación superior: coef. -0.364) y la cultura educativa general (promedio de años de escolaridad en mujeres: coef. +0.035). Por lo que el Apruebo se sostuvo en promedio en sectores de clase media con alta escolaridad.

Para el 2023, se reconfigura el voto, las comunas con mayor cultura educativa en general rechazaron la propuesta (coef. -0.043), mientras que la élite profesional se posicionó por el A Favor (coef. +0.727). El A Favor logró capturar también el voto de un sector vulnerable de la población (+0.88), mientras la clase media actuó como freno. 

Otros hallazgos de las variables de control:

El Giro de la Pobreza:

En 2022, la pobreza fue un predictor de Rechazo (Coef: -0.84).

En 2023, la pobreza fue el motor principal del A Favor (Coef: +0.88).

El Muro Generacional:

Las comunas con predominio de adultos (50-64) votaron sistemáticamente por la opción conservadora en ambos plebiscitos (Rechazo en 2022, A Favor en 2023).

Los resultados de los modelos de regresión logística muestran una confirmación de lo anterior:

Para el Plebiscito de 2022, el modelo presenta coeficientes con errores estándar altos en las variables de edad. Esto indica que en ciertos grupos etarios, el rechazo a la propuesta fue exclusivo. Ninguna comuna de rango etario 50-64 votó apruebo. Por otro lado, hay una tendencia marginal donde a mayor pobreza se redujo la probabilidad de votar Apruebo (P= 0.07, coef: -39.9)

El modelo de 2023 confirma lo anterior también, esta vez, la educación operó en las dos fuerzas. Tener una gran cantidad de personas con educación superior aumentó la probabilidad de una victoria del A Favor, mientras que a mayor promedio de escolaridad de mujeres, disminuye la probabilidad de victoria. Finalmente, la derecha capturó el voto de la población con educación superior, pero pierde fuerza al analizar las características de estas personas.

Otras determinantes claves de estos modelos:

- Pobreza (***): Es el predictor más potente. Un aumento en la pobreza dispara la probabilidad de victoria de la opción "A Favor" (Coef: +22.6).

- Edad (**): El grupo de referencia (Mayores) es la base del triunfo. Los jóvenes (grupo_edad_unido1) muestran un coeficiente negativo significativo (-0.90), lo que indica que es menos probable que gane la opción conservadora en una comuna joven comparada con una vieja.

- Castigo Político (**): Municipios de Izquierda (-0.78) o Independientes (-0.83) redujeron significativamente las chances de éxito de la opción republicana frente a los municipios de derecha.
