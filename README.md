# Master_Thesis
FIJI Macros, R Scripts

The provided FIJI Macros and R Scripts were used mainly to test the functionality of pharmacological compounds on S. lacustris. 
Here, different activators, inhibitors and scavengers were used to analyze different contractile pathways and the effects of nitric oxide on the sponge. 
Image sequences were taken with a camera to analyze the behavior of sponges when exposed to different compounds.
These image sequences were saved as TIF files. 

Folder_Structure
  - explains how the folders, subfolders and files were arranged
  - for some macros and scripts the directories have to be changed 
  - this could help to make it work, otherwise, some files might not be found be the macros and scripts

FIJI_Image_Sequence_Inhibitors
  - can be used to label the image sequence
  - crop the images first
  - check correct directory and range (where the labels will be added)
  - add the correct compound and concentration
  - this macro adds labels and saves an AVI file 


FIJI_Image_Sequence_Inhibitors_Reversibility
  - can be used in the same way as FIJI_Image_Sequence_Inhibitors
  - here, reversibility was tested by an exchange of the medium
  - this macro adds a label for this medium exchange


Ilastik
  - is used to measure the change in area of the sponge's canals during inflations
  - choose 3 labels: yellow = incurrent canals, blue = excurrent canals, red = background and remaining tissue
  - these colors must be used exactly like that, otherwise, the next steps do not work
  - train Ilastik to recognize the canals throughout the entire image sequence
  - export the segmentation mask


FIJI_Segmentation_Measurment
  - can be used to measure the area (in pixels) from the Ilastik Segmentation Mask
  - choose the input (segmentation) and output folder (create new folders for that)
  - run the macro
  - the results should be saved automatically as "Results"
  - this is important for the next steps to work

R_Inhibitor_Testing
  - can be used to analyze the "Results" form previous step
  - plots the area of the canals during the image sequence of the inhibitor testing
  - add the correct directories for the triplicates
  - add the correct name of the compound
  - add the correct time of compound additions (for each of the triplicates)

R_Scavenger_Testing
  - can be used as the other R script
  - this script has additional settings for a scavenger that was used with an inhibitor --> two compounds
