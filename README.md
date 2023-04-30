### PyTorch for Medical Imaging Applications
- Deep Learning in Applications 
- Monai
- Case Studies 

#### [Medical imaging] PyTorch Reference Application to detect lung cancer
CT scans are stored on disks, they contain density information, and the models consume various sub-slices of those 3D arrays. There is a multi-step process to go over the entire chest CT scan to give a patient a lung cancer diagnosis. The 3D CT scans product of the CT instance contains a full 3D scan. We combine that with a module that performs segmentation (flagging voxels of interest), and then group the interesting voxels into small lumps in the search for candidate 'nodules. The 'nodule' locations are combined back with CT voxel data to produce nodule candidates which are examined by nodule classifier whether the are actually nodules in the first place. 
The end-to-end implementation is the process of taking a CT scan and determining whether the patient has a malignant tumor.  With CT alone it might not be apparent therefore we take on more deep dive, and look into the data for each of the individual scans, per-module classifications that can then be combined into a whole patient diagnosis. 
Classify candidate modules as actual modules or non-modules using 3D convolution.
Diagnose the patient using the combined per-nodule classifications.
Similar to the nodule classifier, attempt to determine whether the nodule is benign or malignant based on the imagining data alone.Taking the simple maximum of the per-tumor malignancy predictions, as one tumor needs to be malignant for a patient to have cancer.
https://github.com/almascpdcs224n/__computational-biology/blob/main/__LunaRefApp_with_PyTorch.ipynb

<table>
<tr> <img width="1282" alt="image" src="https://user-images.githubusercontent.com/67139134/235373445-f2756a8b-dc55-404c-a4cc-1688a60c5d26.png">
 <br/></tr>

</table>
