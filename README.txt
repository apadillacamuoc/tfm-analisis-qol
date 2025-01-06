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

"ql" - Estado global de salud/Calidad de vida (QoL) ! "pf" - Funcionamiento físico    ! "rf" - Funcionamiento de roles 
"ef" - Funcionamiento emocional                     | "cf" - Funcionamiento cognitivo | "sf" - Funcionamiento social
"fa" - Fatiga                                       | "nv" - Náuseas y vómitos        | "pa" - Dolor
"dy" - Disnea                                       | "sl" - Insomnio                 | "ap" - Pérdida de apetito
"co" - Estreñimiento                                | "di" - Diarrea                  | "fi" - Dificultades financieras
"brst" - Síntomas en el brazo                       | "brbi" - Imagen corporal        | "brbs" - Síntomas en el seno
"flq" - Escala funcional                            | "brfu" - Perspectiva futura     | "brsee" - Disfrute sexual
"brsef" - Funcionamiento sexual                     | "slq" - Escala de síntomas      | "brhl" - Molestia por la pérdida de cabello
"bras" - Efectos secundarios de la terapia sistémica| 

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

"maritial_status" - Estado civil   | "education" - Nivel educativo   | "alcohol" - Consumo de alcohol | "smokingstatus" - Estado de fumador
"bust" - Tamaño del busto          | "cupsize" - Tamaño de copa      | "menstruation_firsttime_age" - Edad de la primera menstruación
"menopause_yn" - Menopausia (Sí/No)| "birth_number" - Número de hijos| "pregnancy_number" - Número de embarazos 
"comorb_none" - Sin comorbilidades | "comorb_heart" - Comorbilidad: Enfermedad cardíaca | "comorb_hypertension" - Comorbilidad: Hipertensión
"comorb_paod" - Comorbilidad: Enfermedad arterial periférica (PAOD) | "comorb_lung" - Comorbilidad: Enfermedad pulmonar
"comorb_diabetes" - Comorbilidad: Diabetes | "comorb_kidneys" - Comorbilidad: Enfermedad renal
"comorb_liver" - Comorbilidad: Enfermedad hepática | "comorb_stroke" - Comorbilidad: Accidente cerebrovascular
"comorb_neurological" - Comorbilidad: Trastornos neurológicos | "comorb_cancerlast5years" - Comorbilidad: Cáncer en los últimos 5 años
"comorb_depression" - Comorbilidad: Depresión | "comorb_gastrointestinal" - Comorbilidad: Trastornos gastrointestinales
"comorb_endometriosis" - Comorbilidad: Endometriosis | "comorb_arthritis" - Comorbilidad: Artritis
"comorb_incontinence" - Comorbilidad: Incontinencia | "comorb_uti" - Comorbilidad: Infección urinaria (UTI)
"cancer_breast" - Cáncer de mama | "contraceptive_kind" - Método anticonceptivo | "pre_op" - Estado preoperatorio
"cancer_kind_family_1" - Tipo de cáncer en la familia | "breastcancer_first" - Primer diagnóstico de cáncer de mama
"diagnosis" - Diagnóstico | "lateral" - Lateralidad (Derecha/Izquierda) | "histotype" - Tipo histológico
"gradeinv" - Grado de invasión | "erstatus" - Estado de receptor de estrógeno (ER) | "prstatus" - Estado de receptor de progesterona (PR)
"her2status" - Estado de HER2
