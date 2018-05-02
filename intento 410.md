[Hola mundo](https://youtu.be/vy6RdKpYuuo)

# Jupyter



**Historia**

[Jupyter](https://www.youtube.com/watch?v=cxXL5A4u-D8) surge en 2014 como una evolución del proyecto IPython, una potente consola vitaminada para Python. Sin embargo, Jupyter es mucho más ambicioso que IPython, se pretende construir una plataforma agnóstica del lenguaje que ofrezca a los científicos un conjunto de potentes herramientas para trabajar con datos, visualizarlos y poder compartir los resultados.

El origen de su nombre es un homenaje a Galileo, al que se considera autor del primer “paper” científico de astronomía de la era moderna en 1610, en el cual describe sus observaciones astronómicas a través de un telescopio de las lunas de Júpiter. Galileo demostró que la Tierra orbita el Sol de la misma manera que las lunas de Júpiter orbitan dicho planeta.

[![Jupyter2](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter2.jpg)](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter2.jpg)

El proyecto fue iniciado por [Fernando Pérez](https://bids.berkeley.edu/people/fernando-perez), un científico y profesor de la Universidad de California Berkeley. Sin embargo, el proyecto es  **software libre**  y está  **basado en componentes libres**, por lo que está apoyado, desarrollado y mantenido por una amplia [comunidad](http://jupyter.org/about.html).

La adopción y el éxito de Jupyter ha sido muy grande, de tal modo que se está convirtiendo en un standard para el trabajo de los científicos de datos. Hoy en día la herramienta está integrada algunas de las plataformas y entornos más importantes y extendidas como [Google Cloud](https://cloud.google.com/datalab/),[Microsoft Azure](https://azure.microsoft.com/es-es/documentation/articles/virtual-machines-linux-jupyter-notebook/), [AWS](https://blogs.aws.amazon.com/bigdata/post/TxX4BY5T1PQ7BQ/Using-IPython-Notebook-to-Analyze-Data-with-Amazon-EMR), [IBM Bluemix](https://developer.ibm.com/bluemix/2016/03/22/accelerating-data-science-with-jupyter-notebooks-and-spark/), [Databricks Platform](https://databricks.com/blog/2016/02/17/introducing-databricks-community-edition-apache-spark-for-all.html), [GitHub](https://github.com/blog/1995-github-jupyter-notebooks-3), [Rackspace](https://developer.rackspace.com/blog/how-did-we-serve-more-than-20000-ipython-notebooks-for-nature/), Continuum,[Jetbrains](https://www.jetbrains.com/help/pycharm/2016.1/tutorial-using-ipython-jupyter-notebook-with-pycharm.html).

# ¿Cómo funciona Jupyter?

Jupyter nos ofrece una shell interactiva vía web, a la que podemos acceder desde un navegador. La shell está organizada en pequeños bloques, cada bloque puede contener texto arbitrario formateado en [Markdown](https://daringfireball.net/projects/markdown/), fórmulas matemáticas en [LaTeX](https://www.latex-project.org/), código en multitud de lenguajes, resultados, gráficos, vídeos, widgets o cualquier elemento multimedia.

[![](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter3.png)](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter3.png)

Podemos escribir código de programación en estas celdas e ir ejecutándolo paso a paso o todo de golpe, obteniendo todos los resultados parciales. También podemos usar los bloques de texto para documentar el código o añadir las explicaciones oportunas, que pueden contener enlaces, imágenes, vídeos u otros elementos.

Esta serie de piezas de código, notas y resultados se guardan en un notebook, que es un fichero que contiene toda esta información. Uno de los principales objetivos de Jupyter es  **fomentar y simplificar la compartición de conocimiento y resultados a través de los notebooks**. Plataformas como [GitHub](https://github.com/paradigmadigital/demo-jupyter) o [Databricks Community Edition](https://community.cloud.databricks.com/) facilitan esta tarea. De esta manera los notebooks pueden ser fácilmente difundidos y los resultados pueden ser reproducidos y validados en diferentes entornos. Por supuesto esto es muy útil para la divulgación y la formación o en entornos educativos.

Jupyter soporta integración con más de [40 lenguajes de programación](https://github.com/ipython/ipython/wiki/IPython-kernels-for-other-languages) en los que podemos escribir el código de nuestro notebooks, por ejemplo  **Python**,  **R**,  **Scala**,  **Ruby**  o  **Go**. Pero también es fácilmente integrable con herramientas y plataformas de Big Data como [Spark](https://www.paradigmadigital.com/dev/spark-un-destello-en-el-universo-big-data/), lo que permite abstraerse de la complejidad de estas herramientas, aprovechando todo su potencial desde un entorno muy amigable.

Una forma muy sencilla de probar Jupyter es a través de  [Try Jupyter!](https://try.jupyter.org/?__hstc=262827539.95cc96cdd447c743828fbaf5f07346d2.1471938496430.1472472984744.1472545174390.12&__hssc=262827539.10.1472545174390&__hsfp=3852962345), una página hospedada por Rackspace que nos ofrece una instancia de prueba donde podemos ejecutar algunos notebooks de ejemplo o escribir los nuestros propios.

# Arquitectura e instalación

**¿Cómo funciona internamente Jupyter?** Usa un sistema basado en **Kernel**.  Cada Kernel es un motor de ejecución para un lenguaje o plataforma concreta que ejecuta en el servidor. A través de un sistema de colas basado en [ZMQ](http://zeromq.org/) el código que necesita ser ejecutado es enviado al Kernel correspondiente.

Por otro lado, el navegador se comunica con el servidor a través de [Websockets](https://en.wikipedia.org/wiki/WebSocket) para optimizar el tráfico y mejorar la experiencia de usuario en el entorno de trabajo. Los notebooks son persistidos en disco para guardar todos nuestros cambios y resultados.

[![Jupyter4](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter4.jpg)](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter4.jpg)

Podemos ejecutar Jupyter localmente en nuestro sistema.  [Instalarlo](http://jupyter.readthedocs.io/en/latest/install.html) es tan fácil como instalar[Anaconda](https://www.continuum.io/downloads), la plataforma abierta para data science basada en Python, o directamente con la herramienta de instalación de paquetes de Python, Pip: **$ pip3 install jupyter**

También podemos usarlo remotamente conectándonos a un servidor donde esté instalado. Para simplificar este tipo de despliegues tenemos [JupyterHub](https://jupyterhub.readthedocs.io/en/latest/), una extensión orientada a entornos de trabajo compartido donde múltiples usuarios se quieran conectar al mismo servidor.

# JupyterLab: la siguiente generación

El desarrollo y la evolución de Jupyter están más vivos que nunca. En la [SciPy 2016](http://scipy2016.scipy.org/), conferencia sobre Python aplicado al mundo científico, se anunciaron algunas de las  **nuevas características**  de la siguiente generación que será conocida como JupyterLab.

[![Jupyter5](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter5.jpg)](https://www.paradigmadigital.com/wp-content/uploads/2016/08/Jupyter5.jpg)

En esta versión se han incluido notables mejoras en la interfaz, ofreciéndonos un entorno más limpio, rico y flexible basado en widgets drag&drop. También nos ofrece una mejor integración con la shell del sistema, lo que nos simplifica labores como la monitorización.

# Conclusión

Jupyter es una herramienta libre fantástica que se está convirtiendo en el standard en el mundo del análisis de datos. La comunidad que lo impulsa es muy activa y heterogénea, lo que está enriqueciendo el desarrollo y la integración con otras herramientas y plataformas.

Su impacto está siendo tan importante que hasta la prestigiosa revista científica Nature le ha dedicado un [artículo](http://www.nature.com/news/interactive-notebooks-sharing-the-code-1.16261) que incluye una interesante demo interactiva y describe todas las ventajas de utilizar Jupyter en el mundo del análisis de datos científicos.  
