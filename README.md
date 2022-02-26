# Quantization using Tensorflow lite on Coral dev board

Disclaimer : This is a personal archive of a project done in 2020. Code in this project may not be up to date with the currently available version.

<br>

### Quantization overview
<left><img src="https://coral.ai/static/docs/images/edgetpu/compile-workflow.png" width="80%"></left>

Tensorflow Lite supports Post Quantization as follows :  
Float 16 Quantization : model to 16-bit  
Dynamic Range Quantization : weight to 8-bit fixed point  
Full Integer Quantization : model to 8-bit integer  

<br>

### Environment
Device: Google Coral Dev Board  
OS: Mendel Linux 5.0
TensorFlow Version: 2.3 (to support for TensorFlow Lite Converter)

<br>

### Results
First two quantization conversion seems to work fine as model sizes were reduced compared to default model(32bit) as follows :  
Float 16 Quantization : 2x smaller  
Dynamic Range Quantization : 4x smaller  

Full Integer Quantization conversion produced errors  

Inference for the converted models were all unsuccessful.  
'RuntimeError: Unsupported data type in custom op handler' was produced.  

Multiple users were experiencing the same error.  
(link: https://github.com/google-coral/pycoral/issues/1)  

At the time, Coral dev board served demonstration purposes fairly well, but was not optimized to conduct quantization experiments. 
