# Beginner Friendly OpenMined Terminology

<br>

## Introduction
There is nothing easy about what we’re doing here at OpenMined. Likewise, many people within our community are not machine learning engineers professionally. The following is a list of common technical terms one might hear when working inside this community.

<br>

## Table of Contents
- [General Terminology](#general-terminology)
- [Languages and Frameworks](#languages-and-frameworks)
- [Cloud Providers and Deployment](#cloud-providers-and-deployment)
- [OpenMined Projects](#openmined-projects)

<br>

## General Terminology

<br>

#### Function (also called “Method”)
Any block of code that can be run multiple times. For instance:

    // The function
    function addTwoNumbers(a, b) {
      return a + b;
    }

    // "Calling" that function
    addTwoNumbers(1, 2);  // "3"
    addTwoNumbers(7, 9);  // "16"
    addTwoNumbers(1, -2);  // "-1"

Functions exist in all programming languages, although they may look slightly different depending on the language and situation. For all intents and purposes, you can understand a function as “any block of code that can be run multiple times.”

<br>

#### Parameters (also called “Arguments”)
Parameters are the values that you put into a function - in other words, your “input”. These are also sometimes called the function’s “arguments”. In the previous code sample (in the “Functions” section above), we had a function called “addTwoNumbers”. In this case, the parameters for that function were “a” and “b” (they’re always put between the parentheses).

<br>

#### Data Science
Loosely speaking, data science is the study of information, particularly as it relates to digital information. It’s sometimes referred to as the study of the intersection between mathematics, software engineering, and database theory.

<br>

#### Artificial Intelligence (also called “AI”)
Techniques that enable computers to mimic human behavior

<br>

#### Machine Learning (also called “ML”)
A subset of artificial intelligence that uses statistics to help computers improve with experience by trial and error. In other words, you feed a computer some data and it begins to recognize statistical patterns. If you feed it more data, it will begin to improve the accuracy with which it detects existing patterns.

<br>

#### Deep Learning (also called “DL”)
A subset of machine learning that allows you to layer the algorithms used in machine learning to create more accurate predictions or fine-tune the algorithm to be more specific. Deep learning increases the complexity of the calculations significantly, and thus requires powerful computers to be trained effectively.

It’s worth noting that data scientists will often choose to use the graphical processing unit (GPU) in a computer as opposed to the processor (CPU). The GPU is hardware internal to a computer that allows for mathematical calculations to be run very quickly, while a CPU is generally better at delegating tasks.

<br>

#### Federated Learning (also called “FL”)
Traditionally, machine learning algorithms are trained on computers or servers (remote computers that a user can rent) that are very powerful. These can be quite expensive to run and often require very expensive and specific hardware to do so effectively. Likewise, it’s often quite difficult for a data scientist to obtain data unless they work for the company giving them the data to learn from. Often times, the best data on people is found on people’s personal devices: mobile phones, tablets, and computers.

Federated learning is another subset of machine learning that allows people’s devices to train a machine learning (or deep learning) algorithm on the device itself, rather than at a data center. This allows the individual training the algorithm the ability to keep the data on their personal device private, while still allowing the algorithm to learn effectively.

<br>

#### Neural Network (also called “NN”)
A neural network is the combination of multiple “layers” into a graph of multiple algorithms. Think of this as a flow from the left side (your inputs), to the middle (your layers, or graph of algorithms), to the right side (your outputs). You can also think of a neural network as a list of operations for a deep learning network (from left to right):

- Inputs
- Algorithm 1
- Algorithm 2
- Algorithm 3
- Outputs

The image below is a very simple neural network. If you’re still confused, just think of a neural network as “a graph structure that represents how a deep learning network learns”. Think of a “layer” as a single column in that graph.

<div align="center">
    <img alt="Neural Network Diagram" src="/images/nn.png" width="280">
</div>

<br>

#### Model
A model is the resulting data structure that you get from putting data into a neural network - in other words, your “output”.

<br>

#### Training (also called “Learning”)
Training is the process of getting a neural network to learn something. The more data you have, and the better it’s described (or “labeled”, which we will get to later), the more accurate your model is likely to. Your output (model) will always only be as good as your input (data).

<br>

#### Inference (also called “Prediction”)
You can think of inference as the result of putting data into your model to make a prediction. For instance, if I have “trained” a neural network to recognize photos of puppies, I can now ask the neural network “is this picture of my face a picture or a puppy or a picture of something else?” If the neural network is well trained, it will correctly predict that my face is not the face of a puppy - you can say the neural network made an “inference” or a “prediction”.

<br>

#### Raw Dataset (also called “Training Data”)
Your raw dataset, which is more commonly called your “training data” is your input to a neural network in its purest form. Using the puppy example from the “Inference” section above, the raw dataset would be images of animals. Remember, it’s important for a neural network to train on a variety of images, not just images of puppies (sadly).

<br>

#### Labeled Dataset (also called “Labels”)
Your labeled dataset, which is more commonly called your “labels”, is a dataset that mirrors your raw dataset one-to-one, describing what each item in your dataset is. In other words, if I have 5 images in my raw dataset consisting of 3 puppies, 1 parrot, and 1 cat, then my labeled dataset might be: [‘puppy’, ‘parrot’, ‘cat’, ‘puppy’, ‘puppy’]. The order is very important here as each image in the raw dataset must correspond to the label in the exact same order in your labeled dataset.

<br>

#### Validation Dataset (also called “Validation Data” or “Test Data”)
Your validation dataset is a different set of raw data with labels that you set aside explicitly for validating how accurate your model is. For instance, if you have 10,000 photos of animals (with labels, that’s important), then a data scientist may decide to use 6,000 of those photos and labels as their “training dataset” and 4,000 photos and labels as their “validation dataset”. Besides, if you used all 10,000 photos and labels to train on, you’d have no images left to prove that your model actually learned anything! If you show a neural network the same image twice, it won’t tell you what it thinks it might be because it actually knows - you already showed it that image. However, if you show the neural network an image it’s never seen before, then it’s a more statistically “true” test of the accuracy of the model.

<br>

#### Tensor
A tensor is an array of values, which you can think of as an ordered list of numbers. Tensors can also be nested so that can contain many layers of tensors within themselves. These are referred to as the number of “dimensions” to a tensor. Tensors are the technical term for the structure of data that goes in and out of a neural network. If you remember some math from grade school or university, these are also called “matrices” (or a “matrix, singular). Even if the input data of your neural network is a picture of a puppy, the picture will need to first be converted into a tensor. Without going into detail about how to do that, just know that it’s a data structure that a neural network receives and produces and that there are many ways to convert data (pictures, text, financial information, etc.) into tensors so that they may be understood by a neural network.

<br>

#### Overfitting
Overfitting is where a neural network has learned “too much” and is unable to make good predictions. This usually happens when a dataset is too similar. For instance, feeding a neural network 10,000 images of puppies will tell a neural network what a puppy is, but it will not tell a neural network what a puppy isn’t. You can also think of overfitting as “memorization”.

<br>

#### Underfitting
Underfitting is where a neural network hasn’t learned enough and is unable to make good predictions - the opposite of “overfitting”. This usually happens when a dataset doesn’t contain much data on what you’re trying to learn about. For instance, feeding a neural network 10,000 images of puppies will not tell the neural network how to recognize a screwdriver.

<br>

#### Pretrained Model
A pretrained model is a model that has been trained by someone else previously - therefore it should be capable of making a prediction.

<br>

#### Transfer Learning
Transfer learning is the process of taking a “pretrained model” (see above) and continuing the training process further. Sometimes this is to improve the accuracy of the predictions the model is already making. However, sometimes the model is repurposed to do something else entirely. Either way, it’s simply the process of taking a model that’s already been trained for a specific purpose and improving it for your own needs.

<br>

#### Supervised Learning
Supervised learning is where you have a clearly defined input and output. You want a model to receive some data and work towards being able to predict a specific output with the best accuracy possible. There are generally two types of problems in supervised learning: classification and regression.

<br>

#### Classification
Classification is a type of problem in supervised learning where your output needs to fall into a specific category, or “class”. For instance: does this CT scan show the presence of a tumor or not? Or, is this picture a picture of a puppy, cat, bird, or none of those?

<br>

#### Regression
Regression is a type of problem in supervised learning where your output needs to be a specific value. For instance: taking a historical view of stock prices for a given company and trying to predict the stock price of that company in the future.

<br>

#### Unsupervised Learning
Unsupervised learning is where you have a clearly defined input, but you don’t have a specific output. This is where you may need your machine learning model to “discover” patterns in your data. Sometimes this can be helpful when you’re searching for answers in data, but you don’t know the right question to ask. There are generally two types of problems in unsupervised learning: clustering and association.

<br>

#### Clustering
Clustering is a type of problem in unsupervised learning where you try to form categories from patterns in your input data. It’s kind of like “classification”, but where you don’t know what the categories are going to be in advance. Remember that unsupervised learning doesn’t know the output - it needs to figure out the most logical output given whatever input it receives.

<br>

#### Association
Association is a type of problem in unsupervised learning where you try to determine rules from patterns in your input data. This is useful in making predictions about behavior, like a recommendation engine: people who like X product will probably also like Y product... or people who the movie “Pulp Fiction” will probably also like the movie “Jackie Brown”.

<br>

#### Reinforcement Learning (also called “RL”)
Reinforcement learning is where you teach a computer to do a task given certain positive and negative conditions. For instance, if you’re teaching an AI bot in a video game, you’ll need to tell them “you’re allowed to walk on land (positive), but not water (negative), find the quickest way to get from one side to the other”. From there, the model will iterate one step at a time until it figures out the optimal path.

<br>

#### Natural Language Processing (also called “NLP”)
NLP is the process of teaching a machine to make sense of written or spoken language, providing it the ability to figure out a sentence’s structure. NLP can even be used to determine the meaning or emotion related to text: is this speaker being sarcastic?... is this speak talking about Barack Obama when they say “president”?

<br>

#### Computer Vision (also called “Machine Vision”)
Computer vision is the process of teaching a machine to identify objects in the world given a particular image. This is how automated cars learn how to drive or when a computer can tell the difference between different facial expressions.

<br>

#### Generative Adversarial Network (also called “GAN”)
A GAN is a neural network commonly used in generating fake information. This is a fairly new technique and one of the most exciting recent developments in AI. It’s often difficult for a data scientist to get access to quality information that’s properly labeled. Using a GAN, you can synthetically generate this data to use in training or validating a model.

<br>

#### Long Short Term Memory (also called “LSTM”)
One big problem with neural networks is that they operate entirely off of their “short-term memory”, meaning that they are good at following trends in a specific direction. You may say that these models are “accurate, but unwise” - think of Dory from Finding Nemo. LSTM’s are a type of neural network that introduces long-term memory to traditional neural networks. LSTM’s are actually close to the way that human brains remember things - allowing for a core set of beliefs (like human instincts) to modify slightly over time given new information.

<br>

#### Encrypted Machine Learning as a Service (also called “EMLaaS”)
Encrypted machine learning is the core tool that OpenMined provides developers - the ability to encrypt the data or model that they use in training and inference. EMLaaS is the process of deploying encrypted machine learning to a cloud environment where it can be generalized for use by other people. Basically, you can turn machine learning and prediction into a service that you can sell to people, all while protecting the privacy of your model and your data (or other people’s data).

<br>

#### Penetration Testing (also called “Pen Testing”)
Hackers! Pen testing is the process of attempting to hack into a system (intentionally, with the system manager’s permission) so that security holes may be determined. Often, software projects or companies will hire pen testers to intentionally hack their own systems (and pay them well to do it…) so that they may protect themselves better from real-world security attacks. There’s a pen testing team at OpenMined, who tries to break the code our community has written so that we can be confident of deploying our software into production systems.

<br>

#### Gradient Descent
_(Coming Soon)_

<br>

#### Hyperparameter
_(Coming Soon)_

<br>

#### Batching
_(Coming Soon)_

<br>

#### Normalization
_(Coming Soon)_

<br>

#### Confidence Interval (also called “Confidence”)
_(Coming Soon)_

<br>

#### Learning Rate
_(Coming Soon)_

<br>

#### Accuracy
_(Coming Soon)_

<br>

#### Loss
_(Coming Soon)_

<br>

#### Error Rate
_(Coming Soon)_

<br>

#### Back Propagation
_(Coming Soon)_

<br>

#### Forward Propagation
_(Coming Soon)_

<br>

#### Tokenization
_(Coming Soon)_

<br>

#### Homomorphic Encryption (also called “HME” or “HE”)
_(Coming Soon)_

<br>

#### Secure Multi-Party Computation (also called “SMPC”)
_(Coming Soon)_

<br>

#### Differential Privacy
_(Coming Soon)_

<br>

#### Secure Aggregation
_(Coming Soon)_

<br>

#### Plan
A plan is what’s created when you want to turn a function into a string of text. Why would you want to do this? If you’re trying to run machine learning code in two different environments (like a web browser and a server, for instance), the languages that are used in these two environments are going to be different. A plan allows you to zip up your code in one environment and allow it to be understood by another environment. This is, of course, an oversimplification, but just understand that plans are an integral piece of the OpenMined ecosystem.

<br>

#### Protocol
A protocol is a series of plans that allow multiple different users to execute different plans together. The protocol may dictate that 3 different users are to perform 3 different operations and then combine their results at the end. If this is vague, then just understand that, like plans, protocols are integral to the OpenMined ecosystem.

<br>

## Languages and Frameworks

<br>

#### Python
Python is the main language used by data scientists today. It’s used because the language is relatively easy to learn and is visually quite simple and expressive. It also carries very strong library support for mathematical computation through libraries like “NumPy”.

<br>

#### Javascript
Javascript is the main language of the web browser. Traditionally, machine learning is not run in Javascript because of the limited access to computational power that Python and other languages possess. However, since much personal user data is stored and accessed in a web browser by Javascript, it’s the ideal candidate for federated learning. This allows for data to remain in the controls of the user, while also benefitting the data scientist training on their data.

<br>

#### Kotlin
Kotlin is the main language of modern Android development. Java was used to write Android apps for quite some time, but then the Kotlin language was created to address some shortcomings that Java had with respect to Android - particularly with it being so difficult to write. Kotlin is the language used in OpenMined’s federated learning system for Android.

<br>

#### Swift
Swift is the main language of modern iOS development. Objective-C (different from C, and C#, and C++) was used to write iOS apps for quite some time, but then the Swift language was created to address some shortcomings that Objective-C had with respect to iOS - particularly with it being so difficult to write. Swift is the language used in OpenMined’s federated learning system for iOS.

<br>

#### PyTorch
PyTorch is one of the two most popular deep learning frameworks on the planet. Written by Facebook’s AI research team, this framework is the main library extended by the PySyft project. It’s more commonly used in research environments, but can be equally useful in production environments.

<br>

#### TensorFlow
TensorFlow is the other deep learning framework that I mentioned above. It’s written by Google’s AI research team, and is also extended in the PySyft project (under the name “PySyft TensorFlow”). While it’s used more in production environments, TensorFlow is equally useful in research environments.

<br>

#### NumPy
Pronounced “num pie”, NumPy is a mathematics library used in Python. It’s commonly used in machine learning because of how easy and quick it is at implementing common algorithms.

<br>

#### Protocol Buffers (also called “Protobuf”)
Protocol Buffers, or as it’s more commonly known “Protobuf”, is a tool written by Google that allows for data structures to be abstracted away from any one particular language. This allows for similar projects written in multiple languages to have a common format between them (called a “schema”). This cuts down on errors but also cuts down significantly on the code that a developer must write to make their code multi-language or multi-framework compatible.

<br>

## Cloud Providers and Deployment

<br>

#### Amazon Web Services (also called “AWS”)
AWS is the cloud provider from Amazon. While they offer dozens of specific products for specific use-cases, in short, they allow you to write code and run it on their server infrastructure, while paying by the hour, minute, second, or millisecond. This allows for incredible cost savings to developers and eases the path to deployment is not having to maintain your own physical server infrastructure. This is commonly referred to as deployment “to the cloud”.

<br>

#### Microsoft Azure (also called “Azure”)
To avoid defining the phrase again - you can think of Azure as the same thing as AWS, but built by Microsoft.

<br>

#### Google Cloud Platform (also called “GCP”)
To avoid defining the phrase again - you can think of GCP as the same thing as AWS, but built by Google.

<br>

#### DigitalOcean
To avoid defining the phrase again - you can think of Digital Ocean as the same thing as AWS, but built by… DigitalOcean. These guys have been in the web hosting business since before AWS, Azure, and GCP, but they didn’t invent cloud computing (AWS did).

<br>

#### Heroku
To avoid defining the phrase again - you can think of Heroku as the same thing as AWS, but built by Salesforce. It’s a lot easier than most of the other cloud providers.

<br>

#### Docker
Docker is a deployment framework built around the idea of “containers”. Basically a container is an isolated environment where code is run. Often when writing coding you’ll build your software to work with specific other code dependencies, libraries, frameworks, languages, tools, or operating systems. The code you’ve written may not be compatible with other configurations, because it’s a lot of work to even get code working in one configuration let alone dozens of configurations! Containers simplify this process by saying “this is exactly the code, on the exact operating system, running the exact dependencies, in the exact language version, etc… that I specify”. It allows you to isolate the environment that your code will run into one specific environment, which makes deployment very easy.

Before containers, sometimes the software you would write would have a strange reaction to running in a different situation, like on a different operating system. If you develop on a Mac, but deploy to Linux, that change may matter quite a lot to the code you’re writing! Containers force the conditions running the code to be identical no matter where you are… ensuring that deployment is always consistent.

Docker was one of the first major projects to incorporate the concept of “container deployment”, and has now been… “borrowed” by all other major cloud providers.

<br>

## OpenMined Projects

<br>

#### PySyft
PySyft is the main project of the OpenMined community, allowing for developers to write machine learning code in either PyTorch or TensorFlow “flavors” and get the benefits of privacy preservation “for free”. It’s as if PyTorch and TensorFlow were extended to have added privacy and security benefits.

<br>

#### PyGrid
PyGrid does a lot of things, but in short, PyGrid takes PySyft and deploys it to the cloud. This way you can control multiple PySyft workers (for training) at the same time, rather than having to issue commands to each individual machine. PyGrid is also the “coordinator” of OpenMined’s federated learning process, allowing various machines (web browsers and mobile devices) the ability to work together to train a model.

<br>

#### syft.js
Syft.js (which is lowercased when not starting a sentence) is a Javascript “worker library”, meaning that can execute PySyft plans in the browser. This is cool because PySyft has code written in Python, while syft.js only speaks Javascript - they communicate with PyGrid sending messages between them. Another project, Threepio, allows for Python and Javascript to translate messages between themselves so that they can understand each other.

<br>
#### KotlinSyft
KotlinSyft is the Android worker library for PySyft. This means that just like syft.js it can execute PySyft plans and train federated learning models on an Android phone.

<br>

#### SwiftSyft
To avoid having to define the phrase again, SwiftSyft is the same thing as KotlinSyft, but for iOS (written in Swift).

<br>

#### syft-proto
Syft-proto (also lowercased when not starting a sentence) is a project sitting between all other projects in the OpenMined ecosystem. It uses Protobuf (defined above) to create common schemas between the codebases. PySyft, PyGrid, syft.js, KotlinSyft, and SwiftSyft all need to know what a “plan”, “protocol”, and “tensor” are: syft-proto provides the definition for all of these projects so they don’t need to write this code themselves. This has the added benefit of ensuring that all the projects have the exact same organization and that if the definition of a “plan” changes in PySyft, then in changes in all the other libraries automatically. Magic!

<br>

#### Threepio
Threepio is the translation layer between Javascript and Python, but more specifically the translation layer between TensorFlow.js (which is TensorFlow, a Python library, written in Javascript), TensorFlow (Python), and PyTorch (also, Python). Since TensorFlow, PyTorch, and TensorFlow.js all do more-or-less the same thing but in different languages and different styles, it’s important to be able to translate between them.

Javascript can’t understand Python and vice-versa. To get a PySyft plan (using PyTorch) to be understood by Javascript, it must be run through Threepio first, so that syft.js may execute the appropriate commands in TensorFlow.js. If this is still confusing, think of this as a “translation layer between deep learning frameworks in multiple languages”.

<br>

#### Crypten
_(Coming Soon)_

<br>

#### TenSEAL
_(Coming Soon)_

<br>

#### PyDP
_(Coming Soon)_

<br>

#### SyferText
_(Coming Soon)_
