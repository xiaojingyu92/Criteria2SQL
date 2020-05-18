
# Criteria2SQL

Dataset and source code for our work [Dataset and Enhanced Model for Eligibility Criteria-to-SQL Semantic Parsing](http://www.lrec-conf.org/proceedings/lrec2020/pdf/2020.lrec-1.714.pdf).

### Source code (src)
- The implementation based on [SQLova](https://github.com/naver/sqlova). 
#### Requirements
- `python3.6` or higher.
- `PyTorch 0.4.0` or higher.
- `CUDA 9.0`
- Python libraries: `babel, matplotlib, defusedxml, tqdm`
- Example
    - Install [minicoda](https://conda.io/miniconda.html)
    - `conda install pytorch torchvision -c pytorch`
    - `conda install -c conda-forge records`
    - `conda install babel` 
    - `conda install matplotlib`
    - `conda install defusedxml`
    - `conda install tqdm`
- The code has been tested on GTX 1080 Ti running on Ubuntu 16.04.4 LTS.

#### Training and Testing

- To train the model by running:
 `python train.py --seed 1 --bS 2 --accumulate_gradients 8 --bert_type_abb uS --fine_tune --lr 0.001 --lr_bert 0.00001 --max_seq_leng 512` on terminal.

- To test on pre-trained model by running:
 `python test.py --seed 1 --bS 2 --accumulate_gradients 8 --bert_type_abb uS --max_seq_leng 512` on terminal.

- Pre-trained models can be download from [here](https://github.com/naver/sqlova/releases). 

### Dataset (data)
Our dataset derives as [WikiSQL](https://github.com/salesforce/WikiSQL),  while include new types of SQL queries for order-sensitive eligibility criteria, counting-based eligibility criteria, boolean-type eligibility criteria.

###  Citation

If you use Criteria2SQL, please cite the following work:
```
@InProceedings{yu-EtAl:2020:LREC,
  author    = {Yu, Xiaojing  and  Chen, Tianlong  and  Yu, Zhengjie  and  Li, Huiyu  and  Yang, Yang  and  Jiang, Xiaoqian  and  Jiang, Anxiao},
  title     = {Dataset and Enhanced Model for Eligibility Criteria-to-SQL Semantic Parsing},
  booktitle      = {Proceedings of The 12th Language Resources and Evaluation Conference},
  month          = {May},
  year           = {2020},
  address        = {Marseille, France},
  publisher      = {European Language Resources Association},
  pages     = {5831--5839
  }
```
