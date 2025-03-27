# Thesis - Automation of Human Karyotype Analysis Using Image Segmentation and Classification Methods

Human karyotype analysis or karyotype test is the technique used in the field of genetics for conducting a diagnosis, which may help to check one’s chromosomes and identify if there are any genetic problems that cause disorders or diseases. The methods currently used in labs to create karyograms by classification and arrangement are manual, but with the development of machine learning methods, the human karyotype analysis can be automated, which will be more efficient as will take much less time and will be more accurate. Although there are several studies that describe the approaches of the machine learning algorithms with image processing of human karyotype, they suffer from issues such as the lack of data or the limited number of methods used. That only emphasises the need to develop new approaches for the task of karyotype image analysis.

## Dataset

Link to data: https://www.kaggle.com/datasets/aliabedimadiseh/chromosome-image-dataset-karyotype/data	

The data that is being used is the Chromosome Image Dataset from Kaggle. This dataset contains images of a human set of chromosomes, which cytogeneticists use for karyotype analysis. There are XML files with coordinates of boxes which point to the specific chromosome location.

Those images and XML files are used to segment and classify each chromosome from the image. Having extracted them, the next task is detecting if there are any abnormalities like too many chromosomes in one class.

## Methodology

Firstly, to enable karyotype analysis, there is a need for chromosome detection and segmentation using and comparing three object detection models: YOLO, Faster R-CNN, and RetinaNet. Apart from being state-of-art models they are suitable for that task since the dataset (described below) already contains annotations (bounding boxes) for each chromosome of each picture as well. Comparing these three methods will help us determine the most effective detection approach in terms of average precision and average recall on different IoU, and computational efficiency.

When we obtain our segmented chromosomes, each chromosome has to be classified using pre-trained ResNet and VGG models evaluating classification accuracy, precision, and recall to choose the best to classify results in the previous step. 

That combination will help us to create a comprehensive and efficient system for automated chromosome analysis.
