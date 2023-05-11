# Head and Shoulder Classification Project

Project Members: 
	Teng Liang and Frank Li	

Project Goal:
	Our goal is to have a model or several models that will be able to predict whether a stock chart (with 50-80 candles) has a Head and Shoulder pattern, a common stock trading pattern, in the actual graph or not. Instead of using prices to see if the rolling means converge or not, we use the actual price graphs for training and classification. 

## Project Milestones
### Data inquiry and meeting with Fabrice Daniel at CebtrakeSupelec
- Fabrice and his partners had a similar idea a couple of years ago, and they tried to create models that will be able to recognize patterns like head and shoulder, flags, and etc (Stock Chart Pattern recognition with Deep Learning). Our plan was to contact Fabrice and see if there’s anything we can use, such as the dataset of stock patterns that he used. This milestone consists of getting information from Fabrice about his project and formulate our own plan with this new domain knowledge.
Data Collection: We need raw stock price data in csv in order to create our own dataset of Head and Shoulder Patterns. Therefore, we planned to get multiple csvs of raw stock price data before building the program which detect Head and Shoulder Patterns to create our dataset. This milestone is consists of getting the raw stock price data in csv format.

### Data Wrangling/Dataset creation 
- Unlike most easy projects, we need to wrangle and process our data from scratch. Since there are no Head and Shoulder Stock Pattern datasets online, we needed a dataset full of hundreds, if not thousands of images of the Head and Shoulder Pattern. This meant that we needed to create our own dataset. We planned to do this by getting raw stock data from API or websites like TradingView. We first load the data that we collected into pandas data frame. Then, we create functions that will recognize head and shoulder patterns in our time series data. We have two different parameters (tolerance and rolling window) to recognize head and shoulder patterns in our data. After using our functions on the data frames, we got a list of ranges of time that include head and shoulder patterns during those time intervals. Then, we draw them out with matplotlib (see below). After getting the images that have potential head and shoulder pattern, we might hand label them with 1 or 0 (some of the graphs are not really head and shoulder) for classification training.
Data Augmentation: We will apply data augmentation (crop, rotation, scaling, and etc) to have more data for our models.

Example of Head and Shoulder Data Creation:
![candlestick_plot_3675](https://github.com/frankli073/head_shoulder_bots/assets/96670089/8870caf1-de37-48d1-bab8-067d2679f7bf)

Example of Non Head and Shoulder Data Creation:
![candlestick_plot_FX_USDCAD, 1D csv_big_10651](https://github.com/frankli073/head_shoulder_bots/assets/96670089/d196ee20-7ce1-4edb-bd84-38e48420fb4c)

### Model Creating
- We will transfer several models (Resnet 50, Alex Net, and etc) then we train on the images.

### Hyperparameters Tuning
- We test different hyper parameters to get the best result.

## *For Notebooks*
### Data Pre-processing
- Check notebook "pre_processing"
- Creaeted function for head and shoulder recognition

### Modeling
- Alexnet
- Resnet
- GoogLeNet

### Results:
-Alexnet: 90.89%	
-Googlenet: 96.59%  	  
-Resnet: 90.91%

