# Unofficial: FBMS Evaluation Code With Fixes

This repository is an unofficial version of the Freiburg Berkeley Motion
Segmentation evaluation code
([webpage](https://lmb.informatik.uni-freiburg.de/resources/datasets/moseg.en.html),
[code](https://lmb.informatik.uni-freiburg.de/resources/datasets/fbms/pami2013_MoSeg_eval.tar.gz))
that fixes a couple minor issues with the FBMS evaluation code:


1. Read up to 99999 characters per line: Some of my file paths are fairly long,
    and lead to some output lines being more than 500 characters, which causes
    the FBMS code to error. This version reads up to 10k characters per line,
    which should be enough for most cases. (See commit [e7df914](https://github.com/achalddave/fbms-evaluation/commit/e7df9146948f5e7177ecf29a895123378573d4b2)).
2. In MoSegEvalAllPR, read the entire output of MoSegEvalPR. The original code
    searches for up to 500 lines for certain key lines, and errors if it does
    not find them. If you have many regions for a specific sequence, the
    original code will error. (See commit [7fdff53](https://github.com/achalddave/fbms-evaluation/commit/7fdff53fa1d55f6838fa305c6869a18be0324a15))

In particular, we have not changed any code related to the evaluation measure.

# Citation

If you used this program in your research work, you should cite the following
publication:

    Peter Ochs, Jitendra Malik, Thomas Brox
    Segmentation of moving objects by long term video analysis
    IEEE Transactions on Pattern Analysis and Machine Intelligence, 2014.
