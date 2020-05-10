# hydronetworks

## Description
This is a modified version of the [original code](https://github.com/carderne/hydronetworks) developed to make use of update **HydroRIVERS** data that now provide river segment connectivity, flow order and estimated discharge values for all river segments. 

The Jupyter notebook (`example.ipynb`) is developed in sections that:

1. Import necessary layers
2. Exclude low Strahler order rivers
3. Use [rasterio](https://github.com/mapbox/rasterio) to extract attributes from raster
4. Estimate small-scale hydropower potential in the network based on some parameters
5. Save the results as geopackages

Supporting documentation is available in [this](https://github.com/akorkovelos) publication but also on Chris's blog post: [Modelling hydrological networks at massive scale](https://rdrn.me/modelling-hydrological-networks/)

## Installation 

**Install from GitHub**

Download repository directly or clone it to you designated local directory using:

```
git clone https://github.com/akorkovelos/hydronetworks
```

**Requirements**

The code has been developed in Python 3. We recommend installing [Anaconda's free distribution](https://www.anaconda.com/distribution/) as suited for your operating system. Once installed, open anaconda prompt and move to your local "hydronetworks" directory using:

```
> cd ..\hydronetworks
```

In order to be able to run the example.ipynb you should install all necessary packages. "hydropotentialenv.ylm" contains all of these and can be easily set up by creating a new virtual environment using:

```
conda env create --name agrodem_run --file hydropotentialenv.ylm
```

This might take a while.. When complete, activate the virtual environment using:

```
conda activate hydropowerenv
```

With the environment activated, you can now move to the hydronetworks directory and start a "jupyter notebook" session by simply typing:

```
..\hydronetworks> jupyter notebook 
```


You can run ```make test``` in the directory, which will do an entire run through using the test data and confirm whether everything is set up properly.



## Credits

**Original code:** [Chris Arderne](https://github.com/carderne) <br />
**Original Methodology:** [Korkovelos et al](https://www.mdpi.com/1996-1073/11/11/3100) <br />
**Updates, Modifications:** [Alexandros Korkovelos](https://github.com/akorkovelos) 
