# Sleep-Stage-Classification


CREATE VIRTUAL ENVIRONMENT WITH CONDA

conda create -n tinysleepnet python=3.6 //
conda activate tinysleepnet //
pip install -r requirements.txt  //

HOW TO RUN 

python download_sleepedf.py
python prepare_sleepedf.py
python trainer.py --db sleepedf --gpu 0 --from_fold 0 --to_fold 19
python predict.py --config_file config/sleepedf.py --model_dir out_sleepedf/train --output_dir out_sleepedf/predict --log_file out_sleepedf/predict.log --use-best
