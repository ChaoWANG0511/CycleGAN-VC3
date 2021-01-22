# CycleGAN-VC3

run :

1) preprocess_training.py

2) train.py

3) evaluation.py

an implementation of 【CycleGAN-VC3: Examining and Improving CycleGAN-VCs for Mel-spectrogram Conversion】

paper's link : https://isca-speech.org/archive/Interspeech_2020/pdfs/2280.pdf

thanks to https://github.com/jackaduma/CycleGAN-VC2.git, this is the first time I learned to build a complete DL project, learned a lot from jackaduma.

difference: 

1) not using view, using interpolate. Since the VC3 used mel-spectrogram rather than MECP(used in VC2), layers' dimension all changed. And hard-coding some layers' channel is no longer reasonable.

2) not using conv1d, all conv are conv2d ( but kernel_size might = 1* n), as indicated in the paper

3) use melgan as vocoder in data preprocessing, not World

4) add evaluation part : mcd, msd score
