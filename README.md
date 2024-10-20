# NPDI Pornography Database
[![Computer Vision and Image Understanding](https://img.shields.io/badge/Computer%20Vision%20and%20Image%20Understanding-DOI-orange)](http://dx.doi.org/10.1016/j.cviu.2012.09.007)
[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-Paper-blue.svg)](https://scholar.google.com/scholar?as_sdt=2005&hl=en&sciodt=0,5&cites=7836593192753784698,285189684813667859&scipsc=)

This repository contains the information for requesting the data from the paper [Pooling in image representation: The visual codeword point of view](https://www.sciencedirect.com/science/article/abs/pii/S1077314212001737?via%3Dihub). We originally created the repository in 2013 at (inactive) Google sites [https://sites.google.com/site/pornographydataset/](https://sites.google.com/site/pornographydataset/).

The Pornography database contains nearly 80 hours of 400 pornographic and 400 non-pornographic videos. For the pornographic class, we have browsed websites that only host that kind of material (solving, in a way, the matter of purpose). The database consists of several genres of pornography and depicts actors of many ethnicities, including multi-ethnic ones. For the non-pornographic class, we have browsed general-public purpose video network and selected two samples: 200 videos chosen at random (which we called "easy") and 200 videos selected from textual search queries like "beach", "wrestling", "swimming", which we knew would be particularly challenging for the detector (called "difficult"). In the following figure, we illustrate the diversity of the pornographic videos (top row) and the challenges of the “difficult” non-pornographic ones (middle row). The easy cases are shown in the bottom row. The huge diversity of cases in both pornographic and non-pornographic videos makes that task very challenging.

<figure>
    <img src="https://github.com/user-attachments/assets/7c4884cc-6125-4ab3-99aa-89ef33679362" alt="npdiporndatabase" style="width:80%;" />
</figure>


#### Summary of the NPDI Pornography Database

Class | Videos | Hours | Shots per Video
:------------ | -------------: | -------------: | -------------: 
Porn | 400 | 57 | 15.6
Non-porn ("easy") | 200 | 11.5 | 33.8
Non-porn ("difficult") | 200 | 8.5 | 17.5
**All videos** | **800** | **77** | **20.6**

Ethnicity | % of Videos (%)
:------------ | -------------:
Asians | 16
Blacks | 14
Whites | 46
Multi-ethnic | 24

# Data Preprocessing

We preprocess the database by segmenting videos into shots. We used industry-standard segmentation software, the STOIK Video Converter. As is often done in video analysis, a keyframe is selected to summarize the content of the shot into a static image. Although there are sophisticated ways to choose the keyframe, we opted to simply select the middle frame of each video shot. In total, there are 16,727 video segments.

# Evaluation

The experimental evaluation is a classical 5-fold cross-validation. We report the **image classification** performance by using the Mean Average Precision (MAP), and the **video classification** by Accuracy Rate, where the final video label is obtained by majority voting over the images. A confusion table is also used to illustrate the results.

# Disclaimer 

THIS DATABASE IS PROVIDED "AS IS" AND WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, WITHOUT LIMITATION, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. The videos, segments, and images provided were produced by third parties who may have retained copyrights. They are provided strictly for non-profit research purposes. They are limited, controlled, distributed, and intended to fall under the fair-use limitation. We take no guarantees or responsibilities whatsoever arising out of any copyright issue. Use at your own risk.

# Downloads

Signing a license agreement is necessary to access the data (videos, video segments, and frames); you can find the license agreement [here](https://github.com/user-attachments/files/17451758/NPDI-Pornography-Database-License-Agreement.pdf). Please sign it and send to Sandra Avila <sandra [at] ic [dot] unicamp [dot] br>; see also the instructions page in the document for more information. 

To make the comparison possible, the training and test folds are available for download:
- Download the [training folds](https://github.com/user-attachments/files/17451832/training.zip) and [test folds](https://github.com/user-attachments/files/17451835/test.zip) (for videos & video segments/frames)

# Citation
If you make use of the Pornography database, please cite the following reference: 
```
@article{avila2013pooling,
  title={Pooling in image representation: The visual codeword point of view},
  author={Avila, Sandra and Thome, Nicolas and Cord, Matthieu and Valle, Eduardo and Ara{\'u}Jo, Arnaldo De A},
  journal={Computer Vision and Image Understanding},
  volume={117},
  number={5},
  pages={453--465},
  year={2013},
  publisher={Elsevier}
}
```

# Acknowledgments
The authors are grateful to CNPq, CAPES, FAPEMIG and FAPESP, Brazilian research funding agencies, for the financial support to this work.




