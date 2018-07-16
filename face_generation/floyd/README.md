# Udacity ND101 - Deep Learning Foundation Nanodegree

This document contains a guide to help you to start experimenting with [Udacity Deep Learning Nanodegree Foundation](https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101) *Project 5* **as easily as possible** through a Jupyter notebook running on FloydHub.

The code in this project was ported from the official course [repository](https://github.com/udacity/deep-learning/tree/master/face_generation), but only the necessary files to run this specific project were selected. The data used in this project is already available as a FloydHub [dataset](https://www.floydhub.com/udacity/datasets).

## Project 5: Face Generation

In this project, you'll use generative adversarial networks to generate new images of faces.

Follow the next steps to get a jupyter notebook up and running for Project 5:

### 1. Create a FloydHub account

* [Sign up](https://www.floydhub.com/signup) on FloydHub
* Install the floyd CLI on your local machine through these two [steps](https://www.floydhub.com/welcome):

```
$ pip install -U floyd-cli

$ floyd login
# Follow the instructions on your CLI
```

### 2. Clone this project to your local machine

```
$ cd /path/to/your-project-dir
$ floyd clone udacity/projects/face-generation/5
```

### 3. Create your project version on FloydHub
* [Create a project](https://www.floydhub.com/projects/create) on FloydHub and then sync the cloned repository with your new project
```
$ floyd init your-project-name
```

### 4. Run the project through a jupyter notebook

* The `--env` flag specifies the environment that this project should run on, which is a Tensorflow 1.2.0 + Keras 2.0.6 backend environment with Python 3.5.
* The `--data` flag specifies that the mnist dataset should be available at the `/mnist` directory and celeba dataset should be available at the `/celeba` directory
* The `--mode` flag specifies that this job should provide us a Jupyter notebook
* Note that the `--gpu` flag is optional for now, unless you want to start right away to run the code on a GPU machine. Since you'll be exploring and playing around with the code, you might not need a GPU instance right away, so you can avoid that flag now and restart it later with a GPU instance.

```
floyd run \
  --env tensorflow-1.2 \
  --data udacity/datasets/mnist/1:mnist \
  --data udacity/datasets/celeba/1:celeba \
  --mode jupyter \
  --gpu
```

Once the job is started, the jupyter notebook will open in your browser and you are ready to go!

### More about FloydHub platform

* Note that changes you make to the notebook running on Floyd servers are not going to be saved at your local directory, but they are going to be available in the [output](https://www.floydhub.com/udacity/projects/face-generation/5/output) section of your job.
* Once you stop the Jupyter notebook job you were running, from the job page, you can click on [Restart](http://blog.floydhub.com/restart-jupyter-notebook-workflow/?utm_medium=email&utm_source=21sep17) to restart your job exactly how you left it and optionally choosing another environment (CPU or GPU). This is a great way to spend less of your GPU hours if you are working on tasks that does not require a GPU.
* If you need any help check our [documentation](http://docs.floydhub.com/) and [forum](https://forum.floydhub.com/).
