# Distributed Tensorflow 1.0.0 Example 

Updated source code for 1.0.0 from 0.8.0

Using data parallelism with shared model parameters while updating parameters asynchronous. See comment for some changes to make the parameter updates synchronous (not sure if the synchronous part is implemented correctly though).

Trains a simple sigmoid Neural Network on MNIST for 20 epochs on three machines using one parameter server. The goal was not to achieve high accuracy but to get to know tensorflow.

Run it like this: 

First, change the hardcoded host names with your own and run the following commands on the respective machines.

```
pc-01$ python example.py --job_name="ps" --task_index=0 
pc-02$ python example.py --job_name="worker" --task_index=0 
pc-03$ python example.py --job_name="worker" --task_index=1 
pc-04$ python example.py --job_name="worker" --task_index=2 
```

# All the credits to author below
More details here: [ischlag.github.io](http://ischlag.github.io/)
