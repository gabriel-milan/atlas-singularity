Bootstrap:docker  
From:debian:buster

%labels
MAINTAINER Gabriel Gazola Milan

%environment
BASE_DIR=/code
export BASE_DIR

%runscript
# This gets run when you run the image!
source /code/atlas-env/atlas_env/bin/activate

%post  
# This section happens once after bootstrap to build the image.
mkdir -p /code
apt update && apt upgrade && apt install -y vim git
cd /code && git clone https://github.com/gabriel-milan/atlas-env
cd /code/atlas-env && ./generate_envs.sh --pip --saphyra --kolmov --root --prometheus