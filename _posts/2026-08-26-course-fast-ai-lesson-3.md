#  Course.Fast.AI Lesson 3

## Lecture Notes

### Terms
- **Tensors:** Everything in PyTorch is tensors; flexible way to store integers, lists of integers, vectors of them, 2d, 3d arrays, etc.
  - Can calculate derivatives of them
  - 1d tensor (array) = rank 1 tensor
- **Gradient descent:** gradually (‘gradient’) lowering (‘descent’) the output of loss function for some parameters/weights etc. of the model/function
- **Rectified Linear:** a type of infinitely flexible model/function used by most models
  - ‘Rectified linear function’
- **Double Relu:** add two rectified linear functions together
  - Triple relu, etc.
  - You can add as many rectified linears to relus as you want
- **Learning Rate:** hyperparameter determining how fast you want to train your model; the number you multiply your `.grad` values by when tweaking parameters during gradient descent. Neither faster nor slower may be optimal, and usually a balance is good. 

### Deep Learning, Summarized In Two Lines
(Double, triple, etc.) relus are the infinitely flexible functions used by models (i.e. the thing that's 'learning'). These relus need parameters, for which we use gradient descent.

### Misc.
- When people say 'you need linear algebra' for AI they are mostly referring to just matrix multiplication
  - Good visualization: [matrixmultiplication.xyz](matrixmultiplication.xyz)

# Footnotes

[^1]: Astronomenal: astronomically phenomenal
