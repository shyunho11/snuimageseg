# TCIA Pancreas-CT Dataset
* 82 CT Scans for Pancreas Segmentation

The images were processed into nii files using the following script:
```
for i in `ls . | grep PAN`; do 
   echo $i; 
   dcm2niix -vox 1 -z y -o ./data/ -m y -s y -f %n $i
done
```

source:
* https://wiki.cancerimagingarchive.net/display/Public/Pancreas-CT (DICOM)
* https://academictorrents.com/details/80ecfefcabede760cdbdf63e38986501f7becd49 (NIfTI)
