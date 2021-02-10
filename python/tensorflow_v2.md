# tensorflow v2
I use [BERT](https://github.com/google-research/bert) from Google. It is required tensorflow>=1.11.0.
In my environment, CUDA is 10.1 and it requires **tensorflow==2.1.0, 2.2.0, 2.3.0**.  
Tensorflow 1.X.X and 2.X.X are complemently different, so I have to convert it v1 to v2.  

## Rough solution
From tensorflow 2.X.X, there is a convert tool, [**tf_upgrade_v2**](https://www.tensorflow.org/guide/upgrade).  
```  
$tf_upgrade_v2 \  
  --intree /input/v1/dir/ \  
  --outtree /output/v2/dir/ \  
  --reportfile /report/file.txt  
```  

## Individual solution
However, **tf_upgrade_v2** cannot solve all problems.  
For example, `tf.contrib.layers.layer_norm` cannot be converted to v2 (such as `tf.compat.v1.hoge`).   
We have to convert these by ourself [ref](https://stackoverflow.com/questions/60883048/converting-tensorflow-tf-contrib-layers-layer-norm-to-tf2-0):  
```
layer_norma = tf.keras.layers.LayerNormalization(axis = -1)
layer_norma(input_tensor)
```


