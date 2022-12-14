# AWSSageMaker-CustomTFModel
Building and training a custom TensorFlow 2.0 Model on Amazon Sagemaker using Keras

This will be trained in script mode on Amazon SageMaker:

```
tf_estimator = TensorFlow(entry_point='train.py', 
                          role=role,
                          instance_count=1, 
                          instance_type='ml.m4.xlarge',
                          framework_version=tf_version, 
                          py_version='py3',
                          script_mode=True,
                          tags=[{"Key": tagKey, "Value": tagValue}],
                          hyperparameters={
                              'epochs': 30
                          }
                         )
```               