¡BIENVENIDO!

Este es un programa de análisis de datos clínicos de calidad de vida. Esta automatizado de tal manera que solo necesitas cambiar 
ciertos nombres en el primer chunk del documento .Rmd, este archivo incluye las instrucciones de como realizarlo. 

Datos del proyecto:
Nombre: Trabajo de Fin de Máster
Autor: Alan Padilla Campoy
Institución: Universitat Oberta de Catalunya
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1. ARCHIVO

En el directorio guarda tu archivo .xlsx y en el programa .Rmd escribe el nombre en la primera opción. 
Ejemplo: el archivo se llama data.xlsx
```{r}
# Escribe aquí el nombre del archivo .xlsx con el que quieras trabajar.
archivo <- "data.xlsx"
```

2. Variable dependiente

Este programa analiza como ciertos factores afectan a diferentes aspectos de la calidad de vida en general. Para estudiar el entorno
global de salud/Calidad de vida (QoL) designa la variable base como "ql". De lo contrario, escoge una de la siguiente lista. 

```
# Escribe aquí el nombre de la variable dependiente que quieras analizar. Puedes consultar la lista en README.txt
base <- "ql"
```

Lista de variables dependientes:

"ql" - Estado global de salud/Calidad de vida (QoL) | "ef" - Funcionamiento emocional | "cf" - Funcionamiento cognitivo | 
"fa" - Fatiga                                       | "pa" - Dolor                    | "dy" - Disnea                   |                
"brst" - Síntomas en el brazo                       | "brbi" - Imagen corporal        | "brfu" - Perspectiva futura     | 
"brsef" - Funcionamiento sexual                     | "sl" - Insomnio                 | 

3. Variables independientes

Estas variables se usan para explorar visualmente si hay diferencias en la variable dependiente según los subgrupos de estas variables.
Escoje tres de la lista. 

```
# Escribe aquí el nombre de tres variables categoricas independientes que sean de tu interés. Puedes consultar la lista en README.txt
variable.exploracion.1 <- "alcohol" 
variable.exploracion.2 <- "contraceptive_kind"
variable.exploracion.3 <- "education"
```

La lista es la siguiente: 

| "maritial_status" - Estado civil                                   | "education" - Nivel educativo                                  | 
| "alcohol" - Consumo de alcohol                                     | "smokingstatus" - Estado de fumador                            |
|"bust" - Tamaño del busto                                           | "cupsize" - Tamaño de copa                                     | 
|"menopause_yn" - Menopausia (Sí/No)                                 | "pregnancy_number" - Número de embarazos                       |
|"comorb_none" - Sin comorbilidades                                  | "comorb_heart" - Comorbilidad: Enfermedad cardíaca             |
|"comorb_hypertension" - Comorbilidad: Hipertensión                  | "menstruation_firsttime_age" - Edad de la primera menstruación |
|"comorb_paod" - Comorbilidad: Enfermedad arterial periférica (PAOD) | "comorb_lung" - Comorbilidad: Enfermedad pulmonar              |
|"comorb_diabetes" - Comorbilidad: Diabetes                          | "comorb_kidneys" - Comorbilidad: Enfermedad renal              |
|"comorb_liver" - Comorbilidad: Enfermedad hepática                  | "comorb_stroke" - Comorbilidad: Accidente cerebrovascular      |
|"comorb_neurological" - Comorbilidad: Trastornos neurológicos       | "comorb_cancerlast5years" - Comorbilidad: Cáncer últimos 5 años|
|"comorb_depression" - Comorbilidad: Depresión                       | "comorb_gastrointestinal" - Comorbilidad: Enf gastrointestinal |
|"comorb_endometriosis" - Comorbilidad: Endometriosis                | "comorb_arthritis" - Comorbilidad: Artritis                    |
|"comorb_incontinence" - Comorbilidad: Incontinencia                 | "comorb_uti" - Comorbilidad: Infección urinaria (UTI)          |
|"cancer_breast" - Cáncer de mama                                    | "contraceptive_kind" - Método anticonceptivo                   |
| "pre_op" - Estado preoperatorio                                    |"cancer_kind_family_1" - Tipo de cáncer en la familia           |
| "breastcancer_first" - Primer diagnóstico de cáncer de mama        |                                                                |