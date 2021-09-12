# Automatic Speaker Recognition

**Description**

This project aims to apply some basic techniques in signal processing for speaker recognition.

The following is the project workflow:
1. Pre-processing of input audio signal
2. Feature Extraction with LPC/MFCC
3. Feature Matching with LBG
4. Dataset Training
5. User Matching

**Compatibility**

This code has been developed and tested well in Windows with Jupter Notebook (Python) on Visual Studio Code.

>**Special Notes**
> - To fix the warning of a singular matrix whose determinant is zero, we have modified it to peform calculations on pseudo inverse (pinv). Additionally, we have set _r[k][0] = 0.0001_ due to NaN issues coupled with the previous warning.
> Using the above patch may or may not result in loss of accuracy.
> - Conversion from LPC to LPCC has been performed but results are not as expected. Although, feel free to modify the code for testing purposes. Let us know your results !

### Results

On a database size of 8 speakers, both the LPC and MFCC algorithms have observed 100% accuracy. 

**References**
- LPC [literature](http://practicalcryptography.com/miscellaneous/machine-learning/linear-prediction-tutorial/)
- MFCC [literature](http://practicalcryptography.com/miscellaneous/machine-learning/guide-mel-frequency-cepstral-coefficients-mfccs/)
- Auto Correlation technique was taken [from here](https://www.philippe-fournier-viger.com/spmf/TimeSeriesAutocorellation.php)
- K-means clustering [reference](https://www.youtube.com/watch?v=1XqG0kaJVHY&feature=youtu.be)
- This is our reference [code flow](https://ccrma.stanford.edu/~orchi/Documents/speaker_recognition_report.pdf)
- Additional reference papers can found [here](https://github.com/STALFivlabs/ASR/tree/master/Reference%20Papers)
