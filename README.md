# Multi threading image crawler in python 3
## Introduction
Find all the images from a website and download to your project folder. Purpose of this project is to learning coding in Python. Please do not use it to your production server yet.
```python
from Crawler.Page import Page
from Crawler.Image import Image
from Image.Download import Download

if __name__ == '__main__':
    page = Page('http://fdfashionltd.com');
    # fetch all the links (anchor) of this website
    links = page.fetch_links();

    for link in links:
        # fetch all of the images of a web url
        img = Image(link);
        images = img.fetch_links();
        # Download all of the images 
        download = Download(links=links)
        download.start()
```
This code is to demonstrate the flow of the work. Please run main.py code because threading are used there. So program will be completed lot faster than this one.
