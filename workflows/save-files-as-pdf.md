---
title: Save Files as PDF
---

## Jupyter Notebooks

Saving Jupyter Notebooks as PDF can be slightly confusing because there are several options presented in the notebook UI. The recommended method is to choose `File `> S`ave and Export Notebook As...` > `Webpdf`.

```{figure} ../images/download_notebook_webpdf.png
:align: center
:name: Download Jupyter Notebook as Webpdf
```

If you choose to download the ipynb file(s) as HTML then choose the following option,

File > Save and Export Notebook As > HTML

```{figure} ../images/download_notebook_html.png
:align: center
:name: Download Jupyter Notebook as HTML
```

### Embedding Images

When it comes to embedding images in Jupyter notebooks so that it is available as part of PDF, there are various methods to include images. Below are the five options to embed an image of an early Mathematica interface.

#### HTML Image

```html
<img src="mathematica.png" alt="Early Mathematica Interface" style="width: 250px;" class="center"/>
```

This method uses standard HTML to embed an image. It is straightforward and allows for extensive customization through HTML attributes like style and class.

#### Markdown Image

```markdown
![mathematica](mathematica.png)
```

Markdown provides a simple syntax for embedding images. This method is concise and ideal for use in Markdown cells in Jupyter notebooks.

#### Markdown Image with Attachment

```markdown
![mathematica.png](attachment:5265a161-c705-42fc-a3ed-ec1fde427030.png)
``` 

This method is used to embed an image as an attachment within a Jupyter notebook. It references the image by its attachment identifier, which is useful for images embedded directly within the notebook file.

```{warning}
All image links referred as part of the Jupyter Notebook should use *https://* and not *http://*. Serving http content within https pages are referred to as [mixed content requests](https://www.cloudflare.com/learning/ssl/what-is-mixed-content). Modern browsers consider these requests to be a security risk and will refuse to load them when using default security settings.
```

#### IPython Display Module

```python
from IPython.display import display, Image
display(Image(filename="mathematica.png", width=250))\
``` 

The IPython.display module provides functions to display images directly in Jupyter notebooks.


## R and Knitting

For R files, select `File` > `Knit Document` > Select the target folder -> Select the Output Format as PDF to save the PDF version of the file.

 ```{figure} ../images/knitting.PNG
:align: center
:name: Downloading R notebook as a PDF
```

```{figure} ../images/knittingpdf.PNG
:align: center
:name: Knitting a PDF
```
