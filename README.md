# Unsupervized

TODO: correct spelling to unsupervised
TODO: add intro, examples, and other open source project essemtials

Template library of unsupervised learning function for numpy, tensorflow, pytorch, and jax.

Integrate with deeppy.

```python
# math
def softmax(x): ...
def swish(x): ...
def relu(x): ...
def leaky_relu(x, alpha=0.2): ...
def elu(x, alpha=1.0): ...
def selu(x): ...
def sigmoid(x): ...
def tanh(x): ...
def softplus(x): ...
def softsign(x): ...
def hard_sigmoid(x): ...
def hard_tanh(x): ...
def log_softmax(x): ...
def log_sigmoid(x): ...
def log_softplus(x): ...
def log_softsign(x): ...
def exp(x): ...
def expm1(x): ...
def log(x): ...
def log2(x): ...
def log10(x): ...
def log1p(x): ...
def logaddexp(x, y): ...
def logaddexp2(x, y): ...
def clip(x, min_value, max_value): ...

# signal analysis
def fft(x): ...
def ifft(x): ...
def rfft(x): ...
def irfft(x): ...
def hfft(x): ...
def ihfft(x): ...

# probability
def entropy(x, sample_axis=0): ...
class StatefulMeasurement:
  def __init__(self): pass
  def __call__(self, *args, **kwargs): pass
class EntropyStateful(StatefulMeasurement): ...
class CrossEntropyStateful(StatefulMeasurement): ...
class MutualInformationStateful(StatefulMeasurement): ...
class KLDivergenceStateful(StatefulMeasurement): ...

# low-level unsupervized machine learning
class PCA: ...
class LDA: ...
class LSA: ...
class NMF: ...
class UMAP: ...
class TSNE: ...
class ISOMAP: ...
class MDS: ...
class LLE: ...
class LPP: ...

class RollingMean: ...

# Unsupervised ML classics
class KNN: ...  # point half-life = inf by default
class DecisionTree: ...
class DecisionForest: ...

class Clustering: ...
class K_Means: ...
class HierarchialClustering: ...
# TODO add more

class BoltzmanNetwork: ...
class RBM(BoltzmanNetwork): ...
class StackedBoltzman(BoltzmanNetwork): ...
class Helmholtz(BoltzmanNetwork): ...
class HopfieldNetwork: ...

# Research
class SOM: ...  # allow_fission=False, fission_rate=1.0, fission_threshold_dist=0.1
class SOMUniformization: ... # uses SOM points to uniformize input density 

# uses local gradient descent, PCA, or another algorithm 
# to adjust weight matrix s.t. it produces an identity 
# vector output if the input is 'normal' or produces a
# zero vecotr output (which is non-zero during unexpected
# events).
class IdentityNormalization: ...

# Unsupervised deep learning udl

# N(0, 1) default, but exponential or uniform can be specified
class Normalization: ...
class LayerNormalization(Normalization): ...
class BatchNormalization(Normalization): ...

# Features (most optional):
# - identity normalizing + matrix multiplication (required)
# - activation: sigmoid, tanh, relu, softmax, etc. (default: sigmoid)
# - exponential normalizing bias vector
# - L1, L2, L1L2 regularization
# - dropout
# default activation=relu, dropout=0.0, L2_reg=0.001
class MLUP: ...  

class Swapout: ...
class Dropout: ...

class RNN: ...
class GRU: ...
class LSTM: ...

class Conv: ...
class Conv1D: ...
class Conv2D: ...
class Conv3D: ...
class ConvTranspose: ...
class ConvTranspose1D: ...
class ConvTranspose2D: ...
class ConvTranspose3D: ...

class Attention: ...  # knn matching for routing values
class MHA: ...

class CNN: ...
class Transformer: ...

# Bio-inspired
class SORN: ... 
class LeakyIntegrateAndFire: ...

# modules that re-export layers and model classes from keras, torch, and flax

# programming: import from deeppy

# self-supervised
class AutoEncoder: ...
class VAE(AutoEncoder): ...
class Quantization = ... # import from _ depending on framework

# misc
class Stateful: ... # Useful for recursive processing. @Stateful rnn_cell(x, h): ..
```
