# Intel-OpenVINO-Windows-Installation-Code-Snippets
code snippets for Intel's OpenVINO Windows Installation




## Environment Variable Scripts

cd C:\Program Files (x86)\IntelSWTools\openvino\bin\

setupvars.bat


## Model Optimizer Scripts

cd C:\Program Files (x86)\IntelSWTools\openvino\deployment_tools\model_optimizer\install_prerequisites

install_prerequisites.bat


## Installation Verifications Scripts

cd C:\Program Files (x86)\IntelSWTools\openvino\deployment_tools\demo\

demo_squeezenet_download_convert_run.bat

demo_security_barrier_camera.bat


## Image Classification Sample Application Using NCS2

### Neural Network Model Conversion Script

python "C:\Program Files (x86)\IntelSWTools\openvino\deployment_tools\model_optimizer\mo.py" --input_model "C:\Users\Testbed\Documents\Intel\OpenVINO\openvino_models\models\FP32\classification\squeezenet\1.1\caffe\squeezenet1.1.caffemodel" --data_type FP16 --output_dir "C:\Users\Testbed\Documents\squeezenet1.1_FP16"

copy "C:\Users\Testbed\Documents\Intel\OpenVINO\openvino_models\ir\FP32\classification\squeezenet\1.1\caffe\squeezenet1.1.labels" "C:\Users\Testbed\Documents\squeezenet1.1_FP16"

### Sample Application Scripts

cd C:\Program Files (x86)\IntelSWTools\openvino\inference_engine\samples\python_samples\classification_sample

classification_sample.py -i "C:\Program Files (x86)\IntelSWTools\openvino\deployment_tools\demo\car.png" -m "C:\Users\Testbed\Documents\squeezenet1.1_FP16\squeezenet1.1.xml" -d MYRIAD

### Additional Sample Application Scripts Utilizing Multiple NCS2

cd C:\Program Files (x86)\IntelSWTools\openvino\deployment_tools\demo\

demo_squeezenet_download_convert_run.bat -d MYRIAD

demo_security_barrier_camera.bat –d MYRIAD

