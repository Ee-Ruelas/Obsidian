
Introduction: What question are you trying to answer?

Is a logistic regression classifier more efficient than a support vector machine with a non-linear RBF kernel at correctly classifying which type of object it is, based on the features below?

Mean motion, Eccentricity, Inclination, B* Drag Term

Data obtained from space-track.org 

### 1. Hyperparameter Tuning Curves (`hyperparameter_tuning_curves.png`)

This plot proves you did your cross-validation study properly. It shows how the **5-Fold Cross-Validation Accuracy** changes on the y-axis as the regularization parameter $C$ changes on the x-axis (in log scale).

- **The Shape of the Curves:** * At very low values of $C$ (strong regularization), the models are heavily penalized and simpler, which might lead to underfitting.
    
    - As $C$ increases, the models become more flexible and pick up finer boundary shapes between the space objects.
        
    - If accuracy drops at very high $C$ values, it means the model is starting to overfit the training splits and performing worse on the validation folds.
        
- **The "Best" Point:** The peak of each curve represents the optimal $C$ value that `GridSearchCV` automatically selected. You will want to point out this peak in your report as your mathematically justified parameter choice.
    

### 2. Side-by-Side Confusion Matrices (`model_confusion_matrices.png`)

The confusion matrices give you a visual breakdown of exactly where your models succeeded and where they made mistakes on the test set.

Each matrix shows a grid crossing the **True Class** (what the object actually is) against the **Predicted Class** (what the model guessed).

- **The Diagonal (Top-Left and Bottom-Right):** These are your correct predictions.
    
    - _Top-Left:_ Actual Debris correctly classified as Debris.
        
    - _Bottom-Right:_ Actual Payloads correctly classified as Payloads.
        
    - _What to look for:_ You want the numbers/colors along this diagonal to be as high and dark as possible.
        
- **The Off-Diagonal (Top-Right and Bottom-Left):** These are your errors.
    
    - _Top-Right (False Payloads / Type I Error):_ Actual space debris that your model mistakenly guessed was a payload.
        
    - _Bottom-Left (False Debris / Type II Error):_ An active payload that your model mistakenly guessed was debris.
        
    - _What to look for:_ Look closely at which model has fewer numbers in these off-diagonal boxes. If the SVM has fewer errors here than Logistic Regression, it physically proves that a non-linear decision boundary is better at separating orbital trajectories than a straight linear line.
      
      



      Mean Train CV Accuracy  Mean Validation CV Accuracy
1                   0.898870                     0.898091
10                  0.904811                     0.904518
100                 0.911116                     0.909046
1000                0.917507                     0.913818
5000                0.920854                     0.915863
Best C selected: 5000
              precision    recall  f1-score   support

      Debris       0.85      0.91      0.88      3045
     Payload       0.95      0.91      0.93      5757

    accuracy                           0.91      8802
   macro avg       0.90      0.91      0.91      8802
weighted avg       0.92      0.91      0.92      8802

      Mean Train CV Accuracy  Mean Validation CV Accuracy
1                   0.798654                     0.798471
10                  0.798775                     0.798569
100                 0.798775                     0.798520
1000                0.798775                     0.798520
5000                0.798775                     0.798520
Best C selected: 10
              precision    recall  f1-score   support

      Debris       0.86      0.51      0.64      3045
     Payload       0.79      0.96      0.86      5757

    accuracy                           0.80      8802
   macro avg       0.82      0.73      0.75      8802
weighted avg       0.81      0.80      0.78      8802