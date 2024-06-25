# music-gen-aws (main) - DreamBooth

* Meta's music generation module's FAST-API implementation using dreambooth method
* Optimized version of music-gen with lower resources consumption

## Installation

The API is tested on Ubuntu 22.04 environment (Python 3.10.14, CUDA12.3).

For installing, follow these instructions

#### Cloning the Main Repository :
```
git clone https://github.com/UsmanGhani6060/DreamBooth-Git.git
```

#### Navigate to Main Repository :
```
cd DreamBooth-Git
```

#### Creating Virtual Enviromrnt :
```
pip install virtualenv
python3.10 -m venv music-gen-dreambooth
source music-gen-dreambooth/bin/activate
```
#### Installing requirements and dependencies:
```
pip install -r requirements.txt
```
## Run

###download the model

# model drive link
```
pip install gdown
```
```
gdown --folder https://drive.google.com/drive/folders/1lQzBXrre1gTPW6YiPBXw38htRSGoKcQx
```
replace "repo_id" in the app.py file to the path of the above downloaded model

#### To run API deployment on server:
```
uvicorn app:app --reload
```

## Testing and Usage:
After deployment, IP Address of corresponding server will be used for further testing and usage.
* Two parameters will be use (`prompt` and `time`) to send request in `JSON` format via using `Postman` or any other testing tool. 
* `prompt` can be any music text with any instrument, which you want to create.
* 5 different time durations in seconds (`5`, `10`, `15`, `20`, `30`) are set for `time` parameter.
* You can check API parameters and endpoints via adding `/docs` text after corresponding IP of FAST-API after deployment.

#### Input example in JSON file/text:
```
{
  "style" : ["indian traditional"],
  "time" : [15]
}
```
