

# attempt 1
My first training run:
- 2 voices summed together
- there wasn't an n_voices flag yet
'''
python scripts/train.py --config v2 --db_path /scratch/nshaheed/rave_poly/preprocess/ --out_path /scratch/nshaheed/rave_poly/models/ --name vctk_2_voice --channels 1 --gpu 0
'''

todos from this one:
- train with --augment mute --augment compress --augment gain
- make a 4 voice one
- make it with brave!

# attempt 2

using brave and incorporating suggestions from attempt 1:

'''
python scripts/train.py --config brave_poly --db_path /scratch/nshaheed/rave_poly/preprocess/ --out_path /scratch/nshaheed/rave_poly/models/ --name vctk_4_voice_brave --channels 1 --n_voices 4 --gpu 0
'''

# attempt 3 (single voice)
Here I'm just trying to train a VCTK stand-in (i.e. one voice) to get a 1:1 comparison

'''
python scripts/train.py --config brave_poly --db_path /scratch/nshaheed/rave_poly/preprocess/ --out_path /scratch/nshaheed/rave_poly/models/ --name vctk_brave --channels 1 --n_voices 1 --gpu 0
'''
