<a id="top"></a>

<div align="center">

# 🌐 Exploiting Multimodal Knowledge Graph for Multimodal Machine Translation

<p>
  <b>Tianjiao Xu</b><sup>1</sup> &nbsp;
  <b>Xuebo Liu</b><sup>2</sup> &nbsp;
  <b>Derek F. Wong</b><sup>3</sup> &nbsp;
  <b>Yue Zhang</b><sup>4</sup> &nbsp;
  <b>Lidia S. Chao</b><sup>3</sup> &nbsp;
  <b>Min Zhang</b><sup>2</sup> &nbsp;
  <b>Tian Gan</b><sup>1</sup>
</p>

<p>
  <sup>1</sup>Shandong University &nbsp;
  <sup>2</sup>Harbin Institute of Technology, Shenzhen &nbsp;
  <sup>3</sup>University of Macau &nbsp;
  <sup>4</sup>Westlake University
</p>

<p>
  <a href="https://ieeexplore.ieee.org/document/11275894/"><img src="https://img.shields.io/badge/IEEE_TMM-2025-blue.svg?style=flat-square"></a>
</p>

<p>
  <b>A plug-and-play data augmentation framework that leverages multimodal knowledge graphs to enhance multimodal machine translation, especially under low-resource settings.</b>
</p>

</div>

Our implementation is based on [FairSeq](https://github.com/pytorch/fairseq.git). Dataset used in the experiments are [Multi30k](https://github.com/multi30k/dataset) and [IKEA](https://github.com/sampalomad/IKEA-Dataset).

## :rocket: Getting Started
Install the dependencies using pip
```bash
pip install -r requirements.txt
```

The method is designed to be plug-and-play, making it applicable to various low-resource corpora. A multimodal knowledge graph compatible with the specific corpus can be obtained through the execution of either `crawl_direct.py` or `crawl_indirect.py`:

```bash
python crawl_direct.py

python crawl_indirect.py
```

Subsequently, data enhancement can be achieved by utilizing the `generate_pseudo_data.py`:
```bash
python generate_pseudo_data.py
```

For reference purposes, the Multi30k and IKEA datasets enhanced through our methodology have been made available [here](https://pan.quark.cn/s/8c637d4a2572) (password: tSJ2).

## :book: Citation
If you find our paper and code useful in your research, please consider giving a star :star: and citation :book:.

```BibTeX
@inproceedings{mmkg_mmt,
  author       = {Xu, Tianjiao and Liu, Xuebo and Wong, Derek F. and Zhang, Yue and Chao, Lidia S. and Zhang, Min and Gan, Tian},
  title        = {Exploiting Multimodal Knowledge Graph for Multimodal Machine Translation},
  journal      = {IEEE Transactions on Multimedia},
  year         = {2025},
}
```

## License
Code released under the [Apache-2.0](LICENSE) License. Dataset released under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
