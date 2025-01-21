# Lecture 1

## Reading and Writing ROOT files

In this first lecture we will learn how to setup ROOT in your machine and the basics of reading and writing ROOT files. 

### Setting up ROOT

If you want to install ROOT in your machine, you can follow the instructions in the [ROOT website](https://root.cern/install/). In my experience one does not simply install ROOT in their first try, so good luck!

With access to cvmfs on one of the Lab Room machines, you can simply run the following command to setup ROOT:

```bash
setup root
```

### Downloading the data

We will use some pregenerated Monte Carlo events coming from ATLAS for the purpose of this tutorial. You can download this data from [here](XXX). Or you can type the following command in your terminal:

```bash
wget https://www.example.com/data.root
```

This file contains some processed events for top anti-top pair production produced for the latest Run3 centre of mass energy at the LHC. 

### Viewing the contents of the file

We can view the contents of this file by running the following command ```root [options] [file]```. For example:

```bash
root -l mc23_13p6TeV.ttbar_PP8.root
```

Available options are:

| Option | Description                                      |
|--------|--------------------------------------------------|
| -l     | Start ROOT in interactive mode (no startup screen) |
| -b     | Start ROOT in batch mode (no graphics)           |
| -q     | Quit ROOT after processing the file              |
| -x     | Exit ROOT after processing the file              |

I would recommend always using the ```-l``` option to make it load up faster. In the latest versions of ROOT, specially if you install it on your own machine, there is an annoying new feature were it will always try to open a browser window whenever you draw stuff. You can disable this by opening root like ```root -l --web=off [more options] [file]```.


