# Cancer-Net BCa Open Source Initiative

<p align="center">
	<img src="assets/cancernet_logo.png" alt="CancerNet Logo" width="25%" height="25%">
	<br>
</p>

**Note: The Cancer-Net BCa models provided here are intended to be used as reference models that can be built upon and enhanced as new data becomes available. They are currently at a research stage and not yet intended as production-ready models (not meant for direct clinical diagnosis), and we are working continuously to improve them as new data becomes available. Please do not use Cancer-Net BCa for self-diagnosis and seek help from your local health authorities.**

**Cancer-Net BCa is part of the Cancer-Net initiatives, a parallel initiative to the [COVID-Net initiative](www.covid-net.ml).**

<p align="center">
	<img src="assets/process.png" alt="Proposed workflow" width="100%" height="100%">
	<br>
</p>

<p align="center">
	<img src="assets/sample-breast-cancer-cdis.png" alt="photo not available" width="90%" height="40%">
	<br>
	<em>Example DWI images with CDI<sup>s</sup> overlaid for sample patients with breast cancer.</em>
</p>

Breast cancer is the second most common type of cancer in women in Canada and the United States, representing over 25% of all new female cancer cases. Neoadjuvant chemotherapy treatment has recently risen in usage as it may result in a patient having a pathologic complete response (pCR), and it can shrink inoperable breast cancer tumors prior to surgery so that the tumor becomes operable, but it is difficult to predict a patient’s pathologic response to neoadjuvant chemotherapy. In this paper, we investigate the efficacy of leveraging learnt volumetric deep features from a newly introduced magnetic resonance imaging (MRI) modality called synthetic correlated diffusion imaging (CDI<sup>s</sup>) for the purpose of pCR prediction. More specifically, we leverage a volumetric convolutional neural network to learn volumetric deep radiomic features from a pre-treatment cohort and construct a predictor based on the learnt features using the post-treatment response. As the first study to explore the utility of CDI<sup>s</sup> within a deep learning perspective for clinical decision support, we evaluated the proposed approach using the ACRIN-6698 study against those learnt using gold-standard imaging modalities, and found that the proposed approach can provide enhanced pCR prediction performance and thus may be a useful tool to aid oncologists in improving recommendation of treatment of patients. Subsequently, this approach to leverage volumetric deep radiomic features (which we name Cancer-Net BCa) can be further extended to other applications of CDI<sup>s</sup> in the cancer domain to further improve prediction performance.

For a detailed description of the methodology behind Cancer-Net BCa and a full description of the dataset used, please click [here](https://arxiv.org/abs/2211.05308).

If you are a researcher or healthcare worker and you would like access to the **GSInquire tool to use to interpret Cancer-Net BCa results** on your data or existing data, please reach out to a28wong@uwaterloo.ca or alex@darwinai.ca

Our desire is to encourage broad adoption and contribution to this project. Accordingly this project has been licensed under the GNU Affero General Public License 3.0. Please see [license file](LICENSE.md) for terms.

If there are any technical questions after the README, FAQ, and past/current issues have been read, please post an issue or contact:
* amy.tai@uwaterloo.ca
* hayden.gunraj@uwaterloo.ca

## Quick Links
1. Main ACRIN-6698 Archive: https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=50135447
2. Cancer-Net BCa models (Cancer pCR prediction for breast cancer): https://github.com/catai9/Cancer-Net-BCa/blob/main/docs/models.md
3. Cancer-Net SCa models (Cancer detection for skin cancer): https://github.com/jamesrenhoulee/CancerNet-SCa/blob/main/docs/models.md

## Core Cancer-Net BCa Team
* DarwinAI Corp., Canada and Vision and Image Processing Research Group, University of Waterloo, Canada
	* Alexander Wong
* Vision and Image Processing Research Group, University of Waterloo, Canada
	* Amy Tai
        * Hayden Gunraj
    
## Demo
A demo of model inference with the Cancer-Net BCa-A model on a provided demo CDI^s image can be found in `demo.ipynb`.


## Citation

```
@inproceedings{cancer-net-bca
	title = {Cancer-Net BCa: Breast Cancer Pathologic Complete Response Prediction using Volumetric Deep Radiomic Features from Synthetic Correlated Diffusion Imaging},
	author = {Tai, Chi-en Amy and Hodzic, Nedim and Flanagan, Nic and Gunraj, Hayden and Wong, Alexander},
	booktitle = {Conference and Workshop on Neural Information Processing Systems (NeurIPS)},
    	series = {Medical Imaging Meets NeurIPS Workshop (MED-NeurIPS)},
	year = {2022},
	url = {https://arxiv.org/abs/2211.05308}
}
```
