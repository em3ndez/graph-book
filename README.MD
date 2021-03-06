<a href="https://g.co/kgs/pSo6dK" target="_blank"> 
  <img src="https://raw.githubusercontent.com/datastax/graph-book/master/notebooks/images/logos/book-cover.jpg" width="300" ALIGN="RIGHT"/>
</a>
You have found the repository containing the data, loading scripts, and Studio Notebooks that accompany "The Practitioners Guide to Graph Data". We wrote this book and created these examples to be your guide in navigating the space between understanding your data as a graph and using your data as a graph. 

You are also welcome to copy and reuse (with citation) all images from our [public LucidCharts documents](https://www.lucidchart.com/invitations/accept/ac590bc4-1407-422b-9843-bda83e0d0b6c).

&nbsp;

**Content Authors:** 
1. [Denise Gosnell](https://twitter.com/DeniseKGosnell)  
2. [Matthias Broecheler](https://twitter.com/MBroecheler)

**Technical Editors:**
1. [Alex Ott](https://github.com/alexott)
2. [Lorina Poland](https://github.com/polandll)
3. [Daniel Kuppitz](https://github.com/dkuppitz)


## What is in this repository?
This repository contains Studio Notebooks, data, and loading scripts to follow the examples within Chapters 3 through 12 in [The Practitioners Guide to Graph Data](https://g.co/kgs/pSo6dK) . The content is organized as follows:
1. `notebooks/`: All DataStax Studio Notebooks for Chapters 3 through 12. These can be uploaded into DataStax Studio via the Studio Import Tool. (Directions below)
2. `data/ch_x`: The data directory contains a folder per chapter. Within each folder, you will find the data and loading scripts to insert the data into DataStax Graph 6.8 via DataStax Bulk Loader.

The directions below detail how to get started.

## Docker Quickstart
1. Make sure you have [Docker and docker-compose](https://www.docker.com/) and [git](https://git-scm.com/) installed
2. Make sure you are giving Docker enough system resources (we recommend 8GB or more of RAM).
3. Clone this repository: `git clone git@github.com:datastax/graph-book.git`
4. Enter the project directory and run `docker-compose up`
5. When both the Studio and DSE services are running, head over to the [DataStax Studio Home Page](http://localhost:9091/) in your browser and you can start using Notebooks that are setup for each chapter.

## How to use this repository
1. Clone this repository: `git clone git@github.com:datastax/graph-book.git`
2. With DataStax and DataStax Studio [installed and running](#downloading-datastax-graph-and-datastax-studio), go to the [DataStax Studio Home Page](http://localhost:9091/)
3. Upload the Chapter notebook you want to use via the Notebook Upload Tool
4. Follow the directions in the Notebook.
5. (Optional) Set up all chapter examples at once:
    1. Import each chapter notebook into DataStax Studio
    2. Create each graph and graph's schema via the chapter's notebook
    3. Update the DEFAULT_DSBULK_PATH within each chapter's loading file. (All loading scripts are located in `data/ch_x/ch_x_load.sh`)
    4. Run the `data/load_all.sh` script to load all data into each graph.
6. Enjoy your reading!

## Downloading DataStax Graph and DataStax Studio

You will need to download and configure two DataStax products to use this repository: DataStax Graph 6.8 with DataStax Studio and DataStax Bulk Loader

Setting Up DataStax Graph 6.8 via a tarball:
1. Download our distrubition of [DataStax Graph 6.8](https://downloads.datastax.com/#enterprise) and [DataStax Studio](https://downloads.datastax.com/#studio)
2. From your terminal, untar the distributions of DataStax Graph 6.8 and DataStax Studio
```
$ tar -xvzf dse-6.8.0-bin.tar.gz
$ tar -xvzf datastax-studio-6.8.0.tar.gz
```
3. Start DataStax Graph:
```
$ ./dse-6.8.0/bin/dse cassandra -s -g -k
```
4. Start DataStax Studio:
```
$ ./datastax-studio-6.8.0/bin/server.sh
```
5. (Optional) See the DataStax Documentation for any custom configurations of [DataStax Graph](https://docs.datastax.com/en/dse/6.8/dse-dev/datastax_enterprise/graph/graphTOC.html) or [DataStax Studio](https://docs.datastax.com/en/studio/6.8/index.html). This is not necessary for using this repository of examples.

Setting up DataStax Bulk Loader via a tarball:
1. Download our Linux distribution of [DataStax Bulk Loader](https://downloads.datastax.com/#bulk-loader)
2. Untar the distribution:
```tar -xvzf dsbulk-1.5.0.tar.gz```
3. Make note of the path to the top level directory of DataStax Bulk Loader.
4. (Optional) See the [DataStax Documentation](https://docs.datastax.com/en/dsbulk/doc/) for any custom configurations of DataStax Bulk Loader. This is not necessary for using this repository of examples.

## What to do next
1. Let us know what you think [on Twitter](https://twitter.com/Graph_Thinking)
2. Leave our book a [review on Amazon](https://www.amazon.com/Practitioners-Guide-Graph-Data/dp/1492044075)

