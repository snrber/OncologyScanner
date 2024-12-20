# OncologyScanner
Flask application. User uploads PDF. Text is extracted and parsed to JohnSnowLabs' MedicalNerModel, a pre-trained named entity recognition model, that can detect medical terms. Hadoop file management system, running on JDK and Spark for data processing. Spark most compatible with Java 8 and 11.

**Points of interest**: 
- Limited pathology reports for oncology, have started with non-oncology reports first in the meantime.
- Used SparkNLP by JohnSnowLabs, seems to be the superior open-source model.

**Pain points**:
- Package dependancies are incredibly painful to deal with (still bugs).
- Issues with hadoop (file manager) and Spark (engine), that allows SparkNLP to run.
- The mechanisms that SparkNLP uses are not updated at the same time; latest version of hadoop may not be compatible with latest version of Spark.

Update 02/12/2024:
- Able to access Spark NLP via VScode
- Unable to download NER models from JohnSnowLabs due to errors in Hadeoop configuration (Hadoop being phased out regardless)
- Using Google Colab notebook to perform NER of medical terms
- Now using spaCy model "en_ner_bc5cdr_md"
