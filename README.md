# DATA 608 - Project
## Classifying Galaxies with Machine Learning

**Authors:** <br>
Ryan Johnston (https://github.com/astroryan97) <br>
Scott Pellegrino (https://www.linkedin.com/in/rspellegrino/) <br>
Troy Stolz (https://github.com/Salsasharkz) <br>

### Why is Galaxy Morphology Important?
* Strongly correlated with other physical parameters.
  * Tracer of orbital mechanics of the stars inside it.
  * Indicator of star formation.
  * Tells us about nuclear activity inside the galaxy.
  * Stage in its evolution.
  * And more.

### The Data

#### Galaxy Zoo 2
The data is obtained from the [galaxy Zoo website](https://data.galaxyzoo.org/) and this [Kaggle Repository](https://www.kaggle.com/jaimetrickz/galaxy-zoo-2-images). The galaxy Zoo project used many human volunteers to classify ~300,000 galaxies. The galaxy zoo is comprised of composite JPEG RGB images in the g, r, and i bands. These images occupy about 3 Gb of data on disk.

We also obtained these two tables relevant to the Galaxy Zoo 2
* **Galaxy Zoo 1 Data** - gz2_hart16.csv.gz
* **Galaxy Zoo 2 image file mapping** - gz2_filename_mapping.csv

#### Suplemntary Tables

Aggregate additional data from:
* SDSS Metadata for GZ2 (Willett et al., 2013).
  * gz2sample.csv.gz
* Galaxy Zoo 1 Table (Lintott et al., 2008).
  * GalaxyZoo1_DR_table2.csv
* GZ1 - Galaxy Mergers (Darg et al. (2010a,b))
  * target_sdss_dr7_dr8.tsv
* GZ1 - AGN Host Galaxies (Schawinski et al., 2010)
  * schawinski_GZ_2010_catalogue.fits

Info from all of these tables are combined into a new table *modified_galaxy_zoo_2_data.csv*.

#### Relevant Variables

* **Color Indicies** - Difference in magnitudes  (i.e. u - g).
* **Eccentricity** - Approximate shape of galaxy to an ellipse (De Vaucouleurs model).
* **4th Adaptive Moments** - The 4th-order second moments of the object’s intensity.
* **50% Petrosian Radius** - Radius containing 50% of Petrosian flux.
* **90% Petrosian Radius** - Radius containing 90% of Petrosian flux.
* **Petrosian Magnitude** - Flux within a certain number of r Petrosian radii.
* **REDSHIFT** - How far away the galaxy is on the cosmic scale.
* **AGN FLAG** - If the galaxy hosts an Active Galactic Nucleus (AGN).
* **MERGER FLAG** - If the object contains merging galaxies.

### Project Goals
* Use Machine/ Deep Learning and parallelization techniques to train a model to classify galaxies into classes of: 
  * Ellipticals
  * Spirals
  * Irregulars
* If time permits: More in depth classification (sub-categories, mixed categories).

* Using images in conjunction with measured parameters; regression and classification will be combined with computer vision and image detection.
* Use supplementary data to train a decision tree classifier.

* Processing to be done in Python/ Jupyter with the help of Talc and Spark
* Useful Packages:
  * SciKitLearn
  * Tensorflow
  * Keras
  * Astropy

### Anticipated Difficulties

#### Data Quality 
* Images are 424 x 424 and therefore may not be overly useful to classify their galaxies

#### Data Size
* Images alone produce ~54 billion data points if each pixel is considered.
* Computation times over the entire dataset will be lengthy.
* Instances of subsets of the data may be necessary when first constructing our methods.

#### Classification “grey-area”
* The data may suggest that some parameters of a galaxy would be classified as one type, while other parameters of the same galaxy suggest otherwise.


# Read the full Report for final presentation for more details.
