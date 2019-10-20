# UPSA
![](sa.PNG)
# Requirement
python==2.7
## python packages
		nltk
        TensorFlow == 1.3.0
        numpy
        pickle
        Rake (pip install python-rake)
        zpar (pip install python-zpar, download model file from https://github.com/frcchang/zpar/releases/download/v0.7.5/english-models.zip and extract it to POS/english-models)



# run the code:
python source/run.py --exps_dir exps-sampling  --exp_name  test   --use_data_path data/quoradata/test.txt --mode kw-bleu  --N_repeat 1  --save_path sa.txt   --batch_size 1 --gpu 0  --search_size 50

# evaluation script
python  source/evaluate.py --reference_path quora-results/ref.txt  --generated_path  quora-results/gen.txt

# Results
|  |  |
|--|--|
|  |  |

|Model| iBLEU | BLEU | Rouge1 | Rouge2 | MEOTER| 
|--|--|--|--|--|--|
|VAE|8.16|13.96|44.55 | 22.64|20.27|
|lag. VAE|8.73|15.52|49.20 | 26.07|23.28|
| CGMH | 9.94 |15.73| 48.73| 26.12 |24.09|
| UPSA | 12.02 |18.18| 56.51| 30.69 |29.02|






