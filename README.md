# SI-NI-FGSM
This repository contains code to reproduce results from the paper:

**Nesterov Acceralated Gradient and Scale Invariance for Adversarial Attacks (ICLR2020)**

openreview report: [https://openreview.net/forum?id=SJlHwkBYDH](https://openreview.net/forum?id=SJlHwkBYDH)

## REQUIREMENTS

- Python 3.6.5
- Tensorflow 1.12.0 
- Numpy 1.15.4 
- cv2 3.4.2
- scipy 1.1.0

## EXPERIMENTS

The code consists of five Python scripts. You should download the [data](https://drive.google.com/open?id=1CfobY6i8BfqfWPHL31FKFDipNjqWwAhS) and [pretrained models](https://drive.google.com/open?id=10cFNVEhLpCatwECA6SPB-2g0q5zZyfaw) before running the code. Then place the data and pretrained models in [dev_data/](dev_data) and [models/](models), respectively.

### Running the code

- `python mi_fgsm.py`:  generate adversarial examples for inception_v3 using MI-FGSM.
- `python ni_fgsm.py`:  generate adversarial examples for inception_v3 using NI-FGSM.
- `python si_mi_fgsm.py`:  generate adversarial examples for inception_v3 using SI-MI-FGSM.
- `python si_ni_fgsm.py`:  generate adversarial examples for inception_v3 using SI-NI-FGSM.
- `python simple_eval.py`:  evaluate the attack success rate under 8 models including normal training models and adversarial training models.

### Example usage

After cloning the repository you can run the giving attack code to generate adversarial examples and then evaluate the attack success rate.

- Generate adversarial examples:

```
python si_ni_fgsm.py
```

- Evaluate the attack success rate：

```
python simple_eval.py
```

## Acknowledgments

Code refer to: [Momentum Attack](https://github.com/dongyp13/Non-Targeted-Adversarial-Attacks)


