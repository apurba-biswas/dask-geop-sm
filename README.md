Creating a Sagemaker docker image

1. Use coiled to create an ECR repository with environment file
    1. ipython shell, import coiled ….
    2. include awscli, boto3, ipykernel in env build
2. Use docker image in EC3 to create a sagemaker image in Cloud9
    1. get sagemaker executioner role i.e. ROLE ARN and set to env var
    2. provide the docker image in ECR as the sagemaker base image
3. Create AppImageConfig
4. Update domain (add to image to json file)
5. 
6. Use jupyter lab 3 if using dask-extension in sagemaker


Coiled’s Docker file command
 RUN conda env update -n coiled -f environment.yml     && rm environment.yml     && conda clean --all -y     && echo "conda activate coiled" >> ~/.bashrc


