# TCIA Pancreas-CT Dataset
* 82 CT Scans for Liver Tumor Segmentation

The images were processed into nii files using the following script:
```
for i in `ls . | grep PAN`; do 
   echo $i; 
   dcm2niix -vox 1 -z y -o ./data/ -m y -s y -f %n $i
done
```

source:
* https://wiki.cancerimagingarchive.net/display/Public/Pancreas-CT (DICOM-original)
* https://academictorrents.com/details/80ecfefcabede760cdbdf63e38986501f7becd49 (NIfTI-processed)
