# Time-Series-Analysis-Skills
Details my Skills on Time Series Analysis

**I) Introduction and Outline**

**II) Warmup (Optional)**

**III) Time Series Basics**

**A) Time Series Basics Section Introduction**

**B) What is a Time Series?**

**C) Modelling vs Predicting**

**D) Why Do We Care About Shapes?**

**E) Types of Tasks**

**F) Power, Log, and Box-Cox Transformations**

**G) Power, Log, and Box-Cox Transformations in Code**

**H) Forecasting Metrics**

**I) Financial Time Series Primer**

**J) Price Simulations in Code**

**K) Random Walks and the Random Walk Hypothesis**

**L) The Naive Forecast and the Importance of Baselines**

**M) Naive Forecast and Forecasting Metrics in Code**

**N) Time Series Basics Section Summary**

**O) Suggestion Box**

## **I) Introduction and Outline**

This course provides a comprehensive guide to analyzing time series data with Python, combining both classical statistical methods and modern machine learning techniques. It begins with a foundation in time series basics, ensuring that learners new to the subject understand the types of data that qualify as time series, essential transformations, evaluation metrics, and a primer on financial time series concepts like log prices, log returns, and randomness.

In the first major section, the course introduces classic forecasting methods, including Exponential Smoothing (ETS) for handling error, trend, and seasonality, and ARIMA models for more machine learning-like approaches to time series prediction. Practical tools such as ACF, PACF, and Auto ARIMA are explored, along with vector models for analyzing interactions between multiple time-dependent variables.

The second section shifts focus to applying machine learning models to time series data. Techniques such as logistic regression, support vector machines, and random forests are used for both forecasting and classification tasks, with examples like predicting user activity from smartphone accelerometer data. The course then advances into deep learning approaches, covering architectures like CNNs, RNNs, and LSTMs, highlighting their adaptability for sequential data and surprising learners who may already be familiar with these models in other domains.

Finally, the VIP section offers exclusive advanced content. This includes Amazon Forecast for automated, state-of-the-art forecasting with minimal coding, GARCH models for modeling both prices and volatility in financial data, and Facebook’s Prophet for practical time series forecasting. Additional surprise VIP materials are promised, making the course appealing for learners seeking the latest tools and techniques.

## **II)Warmup (Optional)**

This set of warm-up exercises introduces practical coding tasks to prepare learners for time series and financial data analysis. The first task is to use NumPy to generate 1000 random samples from the standard normal distribution (mean zero, variance one). These samples are then visualized both as a time series and as a histogram. The next exercise builds on this by adding a trend line to the noise, encouraging experimentation with different parameters and plotting it as a scatterplot rather than a line chart.

A further step is to compute the cumulative sum of the noise samples and plot the result as a time series. Learners are asked to reflect on what this resembles in the context of time series analysis, hinting at concepts like random walks and financial modeling. Following this, students generate 1000 samples from a multivariate normal distribution with a specified mean vector and covariance matrix, then plot the results as a scatterplot to begin thinking about correlations and relationships between variables.

To deepen understanding, learners calculate the sample mean and sample covariance of these multivariate samples. Instead of using NumPy’s built-in mean and cov functions, they are encouraged to apply the actual formulas manually, reinforcing theoretical concepts that will be crucial later in the course.

The instructor emphasizes that these exercises are not meant to teach Python basics but to apply existing skills directly to statistical and financial problems. Mastery of NumPy, pandas, SciPy, and Matplotlib is assumed and considered essential. Learners are reminded that these prerequisites are freely available to study and highly beneficial. The philosophy is that one cannot expect to jump from learning basic coding syntax to analyzing complex financial or time series data overnight; instead, building a solid foundation is crucial for long-term success.

## **III) Time Series Basics**

**A) Time Series Basics Section Introduction**

This section introduces time series basics and a primer on finance. Many students in this course are particularly interested in time series analysis for financial applications. The section begins by answering the question: What is a time series? Although some students may have preexisting intuition about time series, a concrete definition is provided, along with multiple examples to illustrate potential applications.

Next, the concepts of modeling and predicting are discussed. While many beginners in machine learning often consider these the same, they are actually separate tasks. It is important to understand when each task is being performed and why, as there are situations where one is more relevant than the other.

The importance of understanding the “shape” of data is then addressed. This concept, often overlooked in standard courses and books, is essential for visualizing sequences and images. Being able to intuitively understand the shape of data allows for more effective analysis and interpretation.

The lecture then categorizes different types of time series tasks. These include one-step forecasts, multi-step forecasts, multi-output forecasts, and time series classification. Each approach addresses different predictive or analytical needs.

Data transformations, specifically of the Box-Cox variety, are discussed next. Time series transformations differ from typical machine learning transformations, and understanding their purpose is critical. Forecasting metrics are also introduced. Although time series analysis uses many different metrics, familiarity with them is important for reading research papers and communicating effectively with colleagues.

A Financial Time Series Primer follows, introducing key quantities in finance such as net return, gross return, log return, log prices, adjusted close, and dividends. Understanding these concepts is necessary even though financial time series resemble standard time series in structure.

Practical coding exercises include stock price simulations, providing early hands-on experience. These simulations are foundational for later theoretical discussions, including insights into the random walk and the random walk hypothesis. These concepts highlight what is possible and impossible to forecast in financial time series.

The lecture also covers the naive forecast and the importance of having a baseline model. While it may seem simple compared to advanced machine learning models, the naive forecast often serves as a surprisingly effective benchmark. Practical exercises teach how to implement and evaluate the naive forecast using the metrics previously discussed.

This section combines theory and practical work to provide a solid foundation for advanced topics in time series and financial analysis.

**Notes:**

This section covers time series basics and a primer on finance, with a focus on financial applications. The first topic addresses the question: What is a time series? Although some students may have preexisting intuition about time series, a concrete definition is provided, along with multiple examples to illustrate potential applications.

The next topic distinguishes between modeling and predicting. While these concepts are often thought to be the same, they are actually separate tasks. It is important to identify when each task is being performed and understand its purpose.

The concept of data “shape” is introduced, which is critical for visualization and analysis. Understanding the inherent shape of data allows for intuitive interpretation and is particularly useful in courses involving images and sequences.

Time series tasks are then categorized. These include one-step forecasts, multi-step forecasts, multi-output forecasts, and time series classification. Each approach addresses different predictive needs and applications.

Data transformations, specifically Box-Cox transformations, are discussed. Time series transformations differ from regular machine learning transformations, and understanding their purpose is essential.

Forecasting metrics are also covered. Time series analysis involves numerous metrics, and familiarity with them is necessary for understanding research papers and effective communication.

A Financial Time Series Primer introduces key quantities in finance, including net return, gross return, log return, log prices, adjusted close, and dividends. Understanding these terms is critical for financial time series analysis.

Practical coding exercises include stock price simulations, providing early hands-on experience. These simulations serve as a foundation for further theoretical exploration. The random walk and random walk hypothesis are then introduced, illustrating what is possible and impossible to forecast in time series and finance.

The naive forecast is presented as a baseline model. Although it may appear simple compared to advanced machine learning models, it often provides surprisingly effective results. Practical implementation and evaluation of the naive forecast using appropriate metrics are demonstrated.

This section combines theory and practice to establish a strong foundation for more advanced time series and financial analysis topics.

**Summary:**

This section introduces the fundamentals of time series analysis with a focus on financial applications. We begin by defining what a time series is, reinforced with examples to illustrate its practical applications. Next, we clarify the distinction between modeling and predicting, emphasizing the importance of knowing when to perform each task.

We then explore the significance of understanding the “shape” of data, a concept often overlooked in standard courses but crucial for visualizing images and sequences. The section covers different types of time series tasks, including one-step, multi-step, multi-output forecasts, and time series classification. We also discuss data transformations, particularly Box-Cox transformations, highlighting their unique role in time series analysis.

Forecasting metrics are introduced to help interpret papers and communicate effectively with colleagues. A Financial Time Series Primer follows, covering key concepts such as net return, gross return, log return, log prices, adjusted close, and dividends, which are essential for financial applications.

Practical coding exercises begin with stock price simulations to build early hands-on experience. These simulations lead into theoretical insights on the random walk and the random walk hypothesis, providing understanding of what is possible to forecast.

We then introduce the naive forecast as a baseline model, discussing its practical importance and showing how to implement and evaluate it using the metrics covered earlier.

This section balances theory with practical exercises, setting the foundation for advanced topics later in the course.

**B) What is a Time Series?**

This lecture begins by addressing the basic question: What is a time series? Many students may already have some intuition about time series. Examples include the price of a stock or readings from an EKG. The weather is another simple, everyday example of a time series that everyone can recognize. Time series data is clearly all around us, and one does not need to be a data scientist to understand it intuitively. For the purpose of this class, however, a more specific definition is required.

Some types of data will not be discussed in this class. One example is general sequence data. While time series is a type of sequence data, sequences can encompass much more. For instance, sentences are sequences of words, and techniques from natural language processing are used to handle them. Another example is genomics data, where sequences of letters C and G represent molecules akin to computer programs for living things. Unlike these categorical sequences, time series in this class consists of real-valued observations. It is worth noting, however, that many techniques from this course can also be applied to categorical sequences.

Irregularly spaced recordings are another example of data that will not be covered. For instance, if one checks their heart rate on an Apple Watch inconsistently, recording three times one week and two times the previous week at irregular intervals, such data is not suitable for this course. While some techniques exist for handling irregularly spaced time series, this class focuses on models for discrete-time series sampled at regularly spaced intervals. Therefore, for the purposes of this class, a time series is continuous-valued but discrete in time.

Before concluding, another kind of time series—vector time series—is introduced. Vector time series are common. For example, stock prices of multiple stocks recorded at each point in time form a vector time series. Similarly, a single stock with multiple indicators for each time point also forms a vector time series. Brain signals provide another example. Brain-machine interfaces, although sounding futuristic, already have rudimentary implementations. Neuralink, for example, has developed a minimally invasive machine that implants electrodes in the brain. The brain communicates via electrical signals between neurons, and these electrodes can read voltages from different parts of the brain, signaling various activities.

Theoretically, these signals can be decoded to read thoughts. Experiments have enabled monkeys to control a computer mouse using only their minds. Beyond reading, it is possible to write to the brain as well. Once perfected, this technology could allow humans to acquire information directly into their minds, such as reading a book or learning an instrument without physical interaction. This is an example of a vector time series, as multiple electrodes periodically read voltages, forming multiple related time-dependent observations.

**Notes:**

This lecture begins by addressing the question: What is a time series? Intuitively, examples such as stock prices, EKG readings, or weather data illustrate that time series data is present in everyday life. While intuitive understanding is helpful, a more specific definition is required for this class.

Some types of sequence data will not be discussed. Time series is one kind of sequence data, but sequences also include examples such as sentences in natural language processing or genomic sequences composed of letters C and G. Unlike these categorical sequences, time series in this class consists of real-valued observations. However, many techniques presented can also apply to categorical sequences.

Irregularly spaced recordings, such as inconsistent heart rate measurements from a wearable device, are not covered. This class focuses on discrete-time time series sampled at regularly spaced intervals. Therefore, a time series for this course is continuous-valued but discrete in time.

Vector time series are also introduced. These consist of multiple related series observed at the same points in time. Examples include collections of stock prices across multiple companies, a single stock with multiple indicators, or brain signals recorded from multiple electrodes. Brain-machine interfaces, such as Neuralink, illustrate vector time series in a futuristic context, where electrodes read voltages from different parts of the brain to detect activity. These signals, collected periodically, constitute a vector time series and have applications ranging from controlling a computer mouse with thoughts to potentially sending information to the brain.

**Summary:**

This lecture defines time series as real-valued observations sampled at regularly spaced intervals, distinguishing them from general sequence data such as text or genomic sequences. Irregularly spaced measurements are excluded, and discrete-time, continuous-valued series are the focus. The lecture also introduces vector time series, where multiple related observations are recorded simultaneously, with examples including multiple stock prices or brain signals from electrodes. Applications such as brain-machine interfaces illustrate practical uses of vector time series.

**C) Modelling vs Predicting**

This lecture discusses a somewhat subtle topic. Students who are new to machine learning can often conflate the concepts of prediction and modeling. Most beginners to machine learning understand the need to make predictions, but not so much the need to model.

So what's the difference? Prediction is exactly how it sounds. It's about making predictions or, in other words, trying to guess something which you do not know for sure. This makes intuitive sense. For example, we might want to know whether or not someone will click our ad, we want to know how high or low a stock price will go, or we want to find objects in an image. These are all examples of making predictions.

But what does it mean to model? Modeling gives a functional form to your time series. This is very important. Not only does it tell you how to make predictions, but it also gives you deeper insight into why the time series is the way it is. It helps you answer questions about your time series. For example, you can explain why a time series is mean-reverting, or you can explain why a time series will grow unbounded.

Very importantly, it can also tell you how predictable a time series is. Someone who doesn't know how to model might waste their time trying to predict something which is actually unpredictable. For example, we all know intuitively that trying to predict a coin flip would not be useful. Someone who understands how to model will realize that what they have is unpredictable and won't waste time trying to make better predictions.

In the field of time series, we might call making predictions forecasting. So time series forecasting is the act of making predictions. However, modeling would be time series analysis. In any case, this distinction is not too important for this course, but pay attention to which is which as we go through the course. Understand what you are doing and why you are doing it. Sometimes the goal is to make an accurate forecast, but sometimes the goal is to gain a better understanding of the data we're working with. Modeling is one way to help us do this.

**Notes:**

This lecture discusses a somewhat subtle topic. Students who are new to machine learning can often conflate the concepts of prediction and modeling. Most beginners to machine learning understand the need to make predictions, but not so much the need to model.

So what's the difference? Prediction is exactly how it sounds. It's about making predictions or, in other words, trying to guess something which you do not know for sure. This makes intuitive sense. For example, we might want to know whether or not someone will click our ad, we want to know how high or low a stock price will go, or we want to find objects in an image. These are all examples of making predictions.

But what does it mean to model? Modeling gives a functional form to your time series. This is very important. Not only does it tell you how to make predictions, but it also gives you deeper insight into why the time series is the way it is. It helps you answer questions about your time series. For example, you can explain why a time series is mean-reverting, or you can explain why a time series will grow unbounded.

Very importantly, it can also tell you how predictable a time series is. Someone who doesn't know how to model might waste their time trying to predict something which is actually unpredictable. For example, we all know intuitively that trying to predict a coin flip would not be useful. Someone who understands how to model will realize that what they have is unpredictable and won't waste time trying to make better predictions.

In the field of time series, we might call making predictions forecasting. So time series forecasting is the act of making predictions. However, modeling would be time series analysis. In any case, this distinction is not too important for this course, but pay attention to which is which as we go through the course. Understand what you are doing and why you are doing it. Sometimes the goal is to make an accurate forecast, but sometimes the goal is to gain a better understanding of the data we're working with. Modeling is one way to help us do this.

**Summary:**

This lecture distinguishes between prediction and modeling in time series analysis. Prediction involves making guesses about unknown outcomes, such as stock prices, ad clicks, or object detection. Modeling, on the other hand, provides a functional understanding of the time series, explaining its behavior, predictability, and underlying patterns. Forecasting refers to prediction in time series, while modeling corresponds to time series analysis. Understanding the difference helps determine when the goal is accurate prediction versus gaining deeper insight into the data.

**D) Why Do We Care About Shapes?**

So this lecture is going to answer the question, why do we care about shapes? Well, this is an important question because all of the libraries, we will use work under the assumption that your data has a specific shape. If you store your data in any way you want without conforming to the API of those libraries, well then they just won't work as expected. So getting your shapes right is a must. Furthermore, I find that understanding shapes helps you visualize the data.

Time series are generally very easy to visualize. In fact, you are probably visualizing a time series right now, such as the power of words. However, this becomes a bit more difficult when the time series is multidimensional. So considering the shapes of things helps you think about the data in a more real and physical way.

So the simplest time series is a one dimensional time series, for example, the daily temperature over time. In this case, your data would be a one dimensional array. So if you have a time series of length T, then you would have an array of size T. You can think of this as an array that goes from left to right or from top to bottom. However, this is actually an illusion because in one dimension there is no concept of left and right or top and bottom. This only happens because we're representing a one dimensional thing on a two dimensional screen.

In Pandas, data frames are two dimensional, while series objects are one dimensional. In either of these can be used to store a one dimensional time series. If you use a series, then your series would be a series of length T, but if you use the data frame, then it would be a table with T rows and one column. In other words, T by one.

Now, this is where things might get tricky because technically this isn't required. You might ask why not store it as a one by T instead of a T by one? The answer is because it's typically our convention and it works nicely with the libraries we will use. Now, of course, the data frame is capable of holding multiple columns. So now suppose that you have a multidimensional time series, for example, the daily temperature in multiple cities. And suppose that you have the temperature for cities over a period of T days. Then your data frame would have the shape T by D.

So again, why T by D and not D by T? And again, the answer is because this is what works nicely with the libraries we use. And note that this might actually go against your intuition because when we plot a time series, we typically think of it as going from left to right. But in this case, we store the time series going from top to bottom. So just remember that T by D is the convention.

Now things can become even more tricky. Suppose that we have multiple time series, each with multiple dimensions. For example, suppose we're reading accelerometer data from your smartphone. You'd like to use this data to predict whether the user is walking, sitting or lying down. In this case, you might record acceleration in the X, Y, and Z dimensions. So you have D equals three. And suppose that each recording you take lasts two seconds and you sample at 50Hz. So each recording has 100 samples in total, which means T equals 100.

And of course, this is machine learning. So you're going to have multiple training samples. Suppose that you collect 1 million samples of users walking, sitting or lying down. In this case, we introduce a new letter N which by convention we will use for the number of samples in a dataset. So N equals 1 million. We have 1 million samples of users walking, sitting or lying down. In this case, our convention is to organize our data in an array of size N by T by D. So it's a number of samples by number of time steps by number of dimensions.

Now, again, you might be wondering why not a D by T by N or T by N by D. And again, the answer is because this is what our libraries expect. In other libraries and other languages, things might work a different way. So it's always good to be cognizant of what convention is being used. And that's just part of your job as a data scientist.

So when we say N by T by D recognize that this has three dimensions. In other words, you can think of it like a box in 3D space. I always try to encourage students to automatically think of a box whenever they hear N by T by D. This is because just saying N by T by D can be a bit abstract, but a box is clearly very physical and easy to visualize. So try to make this a reflex in your life will become much easier.

So another reason this is useful is because your computer screen is only two dimensional. So suppose you had a three dimensional array in your computer and then you printed it out. Well, what would happen? The answer is that you would lose this 3D structure because your screen is only 2D. So you can see here that it just looks like nonsense. The printout doesn't give me any insight because it flattens a 3D object onto a 2D screen. This is unlike a 1D array and a 2D array where printing things out can be very useful.

And I always have this motto that I tell students: when in doubt, print it out. This usually always helps, but when you have a 3D array, not so much. But in any case, I hope you agree that thinking of shapes is very helpful both for intuition and also to prevent you from making errors when writing code.

**Notes:**

The lecture begins by addressing the question: why do we care about shapes? This is important because all the libraries we use work under the assumption that data has a specific shape. If data is stored in any arbitrary way without conforming to the API of those libraries, then things will not work as expected. Therefore, getting shapes correct is essential. Moreover, understanding shapes helps in visualizing data, since shapes give a mental picture of how data is structured.

Time series are generally easy to visualize. For example, one can intuitively think of time series like the power of words. However, the visualization becomes more difficult when the time series is multidimensional. Considering shapes allows one to think of data in a more real and physical way.

The simplest form of time series is a one-dimensional time series. For example, daily temperature over time is a one-dimensional array. If the time series has a length of T, then the array has a size of T. One may think of this array as extending from left to right or from top to bottom, but this is actually an illusion, since one dimension has no concept of left, right, top, or bottom. These interpretations only occur because the one-dimensional structure is represented on a two-dimensional screen.

In Pandas, data can be stored in two main ways: Series objects, which are one-dimensional, and DataFrames, which are two-dimensional. Either of these can store a one-dimensional time series. If one uses a Series, then the Series has a length T. If one uses a DataFrame, then the structure has T rows and one column, or in other words, T × 1. While it is technically possible to store data as 1 × T, the convention is to store as T × 1, as it works better with the libraries we use.

DataFrames, of course, can store multiple columns. So when we move to multidimensional time series, such as daily temperature across multiple cities, the shape of the DataFrame becomes T × D, where D is the number of cities or dimensions. The convention of storing time along rows (top to bottom) rather than columns (left to right) is not a strict necessity but is used because it aligns with the expectations of libraries. This might feel counterintuitive since time series are usually plotted left to right, but storing as T × D is the adopted convention.

Things become more complex when we consider multiple multidimensional time series. For example, when recording accelerometer data from a smartphone, we may want to predict whether the user is walking, sitting, or lying down. The accelerometer records acceleration along three dimensions: X, Y, and Z, so D = 3. Suppose each recording lasts two seconds and is sampled at 50 Hz. Then, each recording contains 100 samples in total, giving T = 100.

In machine learning, we generally collect multiple training samples. Suppose that we collect one million samples of users performing activities such as walking, sitting, or lying down. Here we introduce N, which represents the number of samples. So in this case, N = 1,000,000. The convention for organizing this data is to use an array of size N × T × D. This means the data is structured as number of samples by number of time steps by number of dimensions.

One might ask why not arrange it as D × T × N or T × N × D. The answer is again because this is the convention that works with the libraries we use. Different libraries and languages might follow different conventions, so it is always important to be aware of which one is in use. As a data scientist, it is part of your responsibility to pay attention to these conventions.

When we say N × T × D, we are dealing with a three-dimensional array. Conceptually, this can be thought of as a box in three-dimensional space. The lecturer encourages students to automatically visualize a box whenever they see N × T × D. This makes the idea less abstract and much easier to imagine.

Another important point is that a computer screen is two-dimensional. So, if we print a three-dimensional array on the screen, the 3D structure is lost. The printout will simply look like nonsense because it is flattening a 3D structure into 2D. In contrast, printing one-dimensional or two-dimensional arrays can still be very useful because their structures are preserved on a screen.

The lecturer concludes with a motto: when in doubt, print it out. Printing is a helpful debugging tool for 1D and 2D arrays. However, with 3D arrays, it is not as useful. Nonetheless, the main lesson is that thinking carefully about shapes is critical for building intuition and avoiding mistakes when writing code.

**Summary:**

This lecture explains why shapes are crucial in data science and machine learning. Libraries rely on data being structured in specific ways, and failing to adhere to these expectations leads to errors. Understanding shapes also helps visualize and reason about data.

A simple one-dimensional time series, like daily temperature, can be stored as a Series of length T or a DataFrame of shape T × 1. Although data could be stored as 1 × T, the convention is T × 1 because it works better with libraries. When dealing with multidimensional time series, such as temperatures in multiple cities, the convention is T × D—time by dimensions—even if this feels counterintuitive compared to how time is usually plotted.

For more complex scenarios, such as accelerometer data with three axes (X, Y, Z), we extend this to multiple samples. With N samples, each of length T and with D dimensions, the data is stored as N × T × D. This convention is chosen because it matches the expectations of the libraries we use, although other conventions may exist in other contexts.

Thinking of N × T × D as a three-dimensional box is a useful visualization technique. However, printing 3D arrays flattens them into 2D, making them hard to interpret, unlike 1D and 2D arrays where printing is often helpful. The guiding principle is that paying attention to shapes not only builds intuition but also prevents coding mistakes. The lecture closes with the motto: when in doubt, print it out—while reminding that this applies mainly to 1D and 2D arrays.

**E) Types of Tasks**

So in this lecture, we are going to discuss the types of tasks that you can do with time series models. We'll start with the most intuitive task, which for most people is the one step forecast that is given. Why one and why two all the way up to what we would like to predict, Y of T plus one. And so that's what we train our model to do.

As a side note, be aware that in this class we might use X of T or Y of T to represent a time series. So in the context of a long time series, there won't be any difference between using X or Y. In a supervised learning, this is a different story. So just keep this in the back of your mind.

Now, the one step forecast is not the end of the story. In practice, we often want to predict multiple steps into the future. We call this the forecast horizon. This is the length of time into the future that we would like to predict. For example, we might want to predict the sales of each day for the next week. One very realistic example is the weather. Imagine checking the Weather Channel and it only shows the weather one day ahead. This wouldn't be very useful compared to other weather channels.

Now, this is not to say that one step forecasts are not useful. It all depends on context. For example, if you run a brick and mortar shop, you might want to forecast the sales of your products next month from monthly data. In this case, that is a one step forecast. This will help you purchase any inventory you might need to fulfill demand in the next month. And again, this all depends on context. When in doubt, ask your manager or your clients or your stakeholders.

So in this course, we're going to learn two ways in which to produce multi-step forecasts. Method number one is called the incremental forecast, which can be done with any one step predictor. Method number two is called the multi-output forecast, which is limited to only certain models. For example, we'll study ARIMA, which can do one step forecasts but cannot do a multi-output forecast. So let's discuss each of these models more in depth.

For now, suppose that our model is a black box. It can only make a one step forecast. Let's suppose that in order to make this prediction, we use past data points. So given Y of T minus P plus one up to Y of T, we can predict Y of T plus one. Let's call this prediction Y hat of T plus one. But suppose that our forecast horizon is three time steps so H is equal to three. In this case, what we can do is plug in our prediction as an input into our model. So for the next input we’ll pass in Y of T minus P plus two up to Y of T followed by Y hat of T plus one. This will give us Y hat of T plus two.

Now that we have our prediction for Y hat of T plus two, we can take this, plug it into our input again and get Y hat of T plus three. The important thing to recognize is that we are not allowed to use the true values for Y of T plus one and Y of T plus two because the current time is only T. T plus one and T plus two are in the future.

So just to give you a concrete example, suppose that we have Y one, Y two, and Y three. Say P is equal to three. So our model uses three past time points to predict the next point. We'd like to predict Y six. So our forecast horizon is three. Before we can do that, we must find Y hat four. So we use our model, plugging in Y one, Y two, and Y three, and that gives us Y hat four. Now in order to estimate Y five we plug in Y two, Y three, and Y hat four. This gives us Y hat five. Finally we can plug in Y three, Y hat four, and Y hat five, and this will give us Y hat six.

Now you might be wondering why can't you just plug in the true values Y four and Y five in order to estimate Y six? The answer is if you imagine these are days, today is only day three. In order to know the true value of Y four and Y five, we would have to wait until day five. And of course, in some businesses this might be unacceptable. As I always tell students who ask this question, imagine your boss asks you to make a forecast three days ahead. Your answer cannot be “OK, but we just have to wait two days to get an answer.” As always, context is important. So ask your clients or your manager what your forecast horizon really is.

Now, let's talk about method number two. Method number two is the multi-output forecast. Again, imagine that we have a black box model. For some models we will study, we'll see that they are capable of giving us multiple outputs at once. Therefore, if we have a forecast horizon H, then we can simply create a model with H outputs and obtain a forecast for each time step up to H points in the future. As you can see, this is much simpler than building a forecast incrementally.

The final task I want to discuss in this lecture is that of classification. This isn't normally discussed in a traditional time series analysis, but this being a more modern course, it's worth knowing. So in the previous examples, our job was always to predict a number. In machine learning, we call this regression. But what if we'd like to predict a category instead? Again, let's pretend that we are Neuralink. We want to read a user's brain signals and guess whether they are hungry or tired. Hungry and tired are categories, not numbers.

Another example is taking motion readings from a smartphone and trying to guess what the user is doing — walking, sleeping, or sitting down. Again, these are categories, not numbers.

OK, so these are some examples of the types of tasks that we can do with time series analysis. Thanks for listening and I'll see you in the next lecture.

**Notes:**

In this lecture, we discuss the types of tasks that can be performed with time series models. The starting point is the most intuitive task, which is the one-step forecast. This means predicting the value at time Y(T+1). That is what the model is trained to do. As a side note, in this class, X(T) or Y(T) may be used to represent a time series. In the context of a long time series, there is no difference between using X or Y. However, in supervised learning, this distinction matters, so it is worth keeping in mind.

The one-step forecast is not the end of the story, because in practice, we often want to predict multiple steps into the future. The length of time into the future we want to predict is called the forecast horizon. For example, one might want to predict sales for each day of the next week. A very realistic example is weather forecasting. If the Weather Channel only gave predictions for the next day, it would not be very useful compared to other channels that provide forecasts for multiple days.

This does not mean that one-step forecasts are not useful. The usefulness depends on the context. For example, if you run a brick-and-mortar shop and you want to forecast next month’s sales from monthly data, that is a one-step forecast. Such a prediction can help you prepare inventory to meet demand in the coming month. Therefore, the task depends on context, and when uncertain, it is best to ask managers, clients, or stakeholders about the forecast horizon they expect.

In this course, we will learn two ways of producing multi-step forecasts. The first method is called the incremental forecast, which can be performed with any one-step predictor. The second method is called the multi-output forecast, which is possible only with certain models. For example, ARIMA can perform one-step forecasts but cannot directly produce multi-output forecasts.

To explain incremental forecasting, suppose we have a black-box model that can only make a one-step forecast. The model uses past values, from Y(T-P+1) to Y(T), to predict Y(T+1). This prediction is called Ŷ(T+1). If the forecast horizon is three (H = 3), we can plug this predicted value back into the model as input. So for the next step, the input becomes Y(T-P+2) through Y(T), followed by Ŷ(T+1), which produces Ŷ(T+2). Similarly, plugging in the new prediction produces Ŷ(T+3). Importantly, we are not allowed to use the true values of Y(T+1) and Y(T+2), since those are in the future and not yet observed.

For a concrete example, suppose we have values Y1, Y2, and Y3, and the model uses three past time points (P = 3) to predict the next one. If the goal is to forecast Y6 with a forecast horizon of three, we first predict Ŷ4 using Y1, Y2, and Y3. Next, to predict Ŷ5, we use Y2, Y3, and Ŷ4. Finally, to predict Ŷ6, we use Y3, Ŷ4, and Ŷ5. Some may ask why we cannot simply use the true values Y4 and Y5 to predict Y6. The answer is that if these values correspond to days, today is only day 3. We cannot know Y4 and Y5 until days 4 and 5 arrive. Waiting is often not an option in business contexts. For instance, if a boss asks for a three-day forecast, it is not acceptable to respond, “We just have to wait two more days.” Thus, understanding the forecast horizon in the context of the problem is critical.

The second method is multi-output forecasting. In this approach, certain models can directly produce multiple predictions at once. If the forecast horizon is H, then the model is designed to produce H outputs, each corresponding to a future time step. This is simpler than incremental forecasting because it avoids repeated inputting of predictions into the model.

The final task covered in this lecture is classification. While not part of traditional time series analysis, classification is important in modern contexts. In previous examples, the task was always regression, where the goal is to predict a number. In classification, however, the goal is to predict a category. For instance, a company like Neuralink might read brain signals and try to predict whether a user is hungry or tired. These outputs are categories rather than numbers. Another example is using smartphone motion data to predict whether a user is walking, sleeping, or sitting down. Again, the outputs are categories, not continuous values.

Therefore, the lecture concludes by emphasizing that time series tasks can include one-step forecasting, multi-step forecasting (incremental or multi-output), and classification. These represent the wide variety of tasks that can be done with time series models.

**Summary:**

This lecture explains the different types of tasks possible with time series models. The most basic task is the one-step forecast, where the model predicts Y(T+1) based on past values. While this is useful in some contexts, many real-world applications require predictions for multiple time steps into the future. The length of time we want to predict ahead is called the forecast horizon. Examples include predicting sales for a week or forecasting the weather for several days.

Multi-step forecasting can be approached in two ways. The first method, incremental forecasting, uses a one-step predictor repeatedly by feeding its own predictions back as inputs to predict further into the future. This method is flexible but accumulates error as predictions are reused. The second method, multi-output forecasting, uses certain models that can directly produce multiple outputs for a forecast horizon in one step. This approach is simpler but only works with specific models.

A concrete example shows how incremental forecasting works with three past data points to predict future points. Importantly, true future values cannot be used during forecasting, as they are not yet observed. This highlights the practical necessity of forecasting without relying on unavailable information.

The lecture also introduces classification as a modern time series task. Unlike regression, which predicts numerical values, classification predicts categories. Examples include detecting hunger or fatigue from brain signals or recognizing whether someone is walking, sleeping, or sitting from smartphone motion data.

In conclusion, time series analysis supports a range of tasks: one-step forecasts, multi-step forecasts (either incremental or multi-output), and classification. Each task is useful depending on the context, and understanding which task to perform is an important part of time series modeling.

**F) Power, Log, and Box-Cox Transformations**

So in this lecture, we are going to discuss some common time series transformations. If you're familiar with machine learning, then you know that it's often useful to transform your data before passing it into a machine learning model. For example, standardization or min scaling. For time series, we'll be discussing three common transformations — the power transform, the log transform, and the Box-Cox transform. As you'll see, these all essentially serve the same purpose.

So let's start with the power transform. The power transform involves raising all your data points to a power. For example, by raising every data point to the power of one half, you'll be taking the square root of your dataset. So why is this useful? Well, imagine that your data appears to grow quadratically in time. If you take the square root, the result would be that you transform your data to grow linearly. So why is that useful? Well, you'll soon learn about some machine learning models that can learn linear trends very well, but there's no model for quadratic trends or cubic trends and so forth. Thus, by transforming your data to appear like it has a linear trend, you give your model a better chance of forecasting future data points and modeling the true nature of the time series more closely.

So another transformation with a similar purpose is the log transform. Like the power transform, it basically ends up squashing your data into a smaller range. In fact, a lot of the time I'll just end up using the log transform by default without considering other options. One common application of the log transform is in finance. In finance, it's common to model stock prices as following a normal distribution. It's also common to model log returns instead of returns based on percentages. As an example, this is the basis for the famous Black-Scholes formula. Note that one possible issue with the log transform is that it doesn't accept zero or negative values as input. For this reason, it can only be used for data which is strictly positive. For data that might be non-negative, it's common to simply add one before taking the log.

OK, so a third transform we're going to discuss is the Box-Cox transform, which generalizes the concept of both the power transform and the log transform. You can see that it involves this parameter lambda, which is the power to use when taking the transform. So why does this make sense? This makes sense because the natural logarithm is actually the limit of this specific power transform as the power approaches zero. Now, inside the Box-Cox function it will automatically choose the value of lambda for us. So we don't need to worry about finding the optimal value ourselves. But if you're interested in learning how this value is chosen, I'd encourage you to check out the SciPy documentation as well as the article I've included in extra reading.

So one common reason people give for why they use the Box-Cox transform is that they want to make the data normally distributed. However, note that this motivation does not apply to raw time series. So why is this? Well, remember that time series data is dynamic. It changes in time. It can have a trend. So when you take time series data and plot a histogram hoping that it will be normal, this is actually the wrong thing to do. We'll discuss this more later in the course. But in order to take data over time and plot its distribution or histogram, we need that data to be stationary. Stationary essentially means its distribution doesn't change over time.

So why is this a requirement? Well, imagine you have some data which simply follows a line that grows at a constant rate. Does plotting the histogram of this data make sense? The answer is no. Would we want this to be normally distributed? The answer is no. In fact, this data behaves much better with a linear trend. The point of plotting a histogram is to understand the distribution of the data, but the distribution at the bottom of this plot is clearly different from the distribution at the top of this plot. Therefore, it makes no sense to mix this data together into a single histogram. This does not tell us how the data is distributed.

The final topic I want to discuss in this lecture is why the log transform is deeply fundamental. Not only is it useful mathematically, but it also seems to be part of nature itself. One example of this is perception. For example, although a normal conversation is ten thousand times louder than a whisper, it doesn't have ten thousand times the effect on your senses. That's why we use the decibel scale to measure sound, which is essentially a log transform.

Another example of how the logarithm seems to simply be a part of nature is how we as humans interpret numbers. For example, if you have one thousand dollars in the bank, then losing one thousand dollars would be a pretty big deal. But if you have one billion dollars in the bank, spending one thousand dollars on a pair of jeans would feel completely normal. Another way to think of this is imagine going from zero dollars in wealth to one million. That's a pretty big jump. How about one million to two million? Although you still made the same amount of money, its utility is less. So one might model the utility of wealth as the logarithm of the wealth.

**Notes:**

In this lecture, we discuss some common time series transformations. If you are familiar with machine learning, you know that it is often useful to transform data before passing it into a model. For example, standardization or min scaling are typical preprocessing steps. For time series, three common transformations are the power transform, the log transform, and the Box-Cox transform. All of these essentially serve the same purpose of reshaping the data in a way that makes it easier for models to learn patterns.

The first transformation is the power transform. This involves raising all data points to a power. For example, raising every data point to the power of one-half corresponds to taking the square root of the dataset. This is useful because if data grows quadratically over time, taking the square root transforms it into something that grows linearly. This is important since many machine learning models can handle linear trends well, but there are no models that can directly capture quadratic or cubic trends. By transforming data to resemble a linear trend, we give models a better chance to forecast accurately and capture the underlying nature of the time series.

Another transformation with a similar purpose is the log transform. Like the power transform, it squashes the data into a smaller range. In practice, it is often used as the default transformation. A common application of the log transform is in finance, where stock prices are often modeled as normally distributed and where log returns are modeled instead of percentage returns. The famous Black-Scholes formula is based on this concept. One limitation of the log transform is that it cannot accept zero or negative inputs, so it can only be applied to strictly positive data. For non-negative data, a common practice is to add one before applying the log.

The third transformation is the Box-Cox transform, which generalizes both the power transform and the log transform. It introduces a parameter lambda, which specifies the power used in the transform. This makes sense because the natural logarithm is the limiting case of the power transform as the power approaches zero. The advantage of Box-Cox is that it can automatically select an appropriate lambda, so we do not need to determine the best value ourselves. For those interested, resources such as the SciPy documentation and extra reading provide more details on how this selection is made.

A common reason given for using the Box-Cox transform is the desire to make data normally distributed. However, this motivation does not apply directly to raw time series data. This is because time series data is dynamic, changes over time, and may have trends. For example, if we plot a histogram of raw time series data, hoping it is normally distributed, we are actually misapplying the idea. In order to examine the distribution of data meaningfully, the data must be stationary, which means that its distribution does not change over time.

To see why this is important, imagine data that follows a line with a constant growth rate. Does plotting a histogram of such data make sense? The answer is no. Should we want this data to be normally distributed? Again, the answer is no. Such data is better represented by its trend rather than its distribution. A histogram is meant to capture the distribution of data, but if the lower part of the time series has a different distribution than the upper part, then combining them into a single histogram is misleading and uninformative. Thus, using Box-Cox or log transforms for the purpose of normalizing raw time series is misguided unless stationarity is first considered.

The lecture then emphasizes why the log transform is deeply fundamental. It is not only useful mathematically but also appears to be built into the nature of perception and human behavior. For example, sound perception is logarithmic. Although a normal conversation is ten thousand times louder than a whisper, it does not have ten thousand times the effect on our senses. This is why sound is measured in decibels, which essentially use a log scale.

Another example is human interpretation of wealth. If you have one thousand dollars, losing that amount is a very big deal. But if you have one billion dollars, spending one thousand on jeans feels insignificant. Similarly, going from zero to one million dollars is life-changing, whereas going from one million to two million is still a large gain but its utility is much less. Thus, the utility of wealth can be modeled using the logarithm of wealth. These examples show how the log transform captures patterns that align with both mathematics and nature.

**Summary:**

This lecture focuses on common transformations for time series data: the power transform, the log transform, and the Box-Cox transform. These transformations are used to reshape data so that machine learning models can better capture trends. The power transform raises data to a power, such as the square root, which can convert quadratic growth into linear growth, making the data easier to model. The log transform similarly compresses data into a smaller range and is widely used in finance, such as modeling stock prices and log returns. However, the log transform only works on positive values, so adjustments like adding one are sometimes necessary.

The Box-Cox transform generalizes these ideas by introducing a parameter lambda that controls the transformation. The log transform itself can be seen as the limiting case of the power transform as lambda approaches zero. Box-Cox is useful because it can automatically choose the value of lambda, relieving the user from manually tuning it. Although many use Box-Cox to try to make data normally distributed, this reasoning does not apply to raw time series data. Because time series are dynamic and may include trends, their distributions change over time. Stationarity is a requirement for examining distributions meaningfully, and histograms of non-stationary time series can be misleading.

The lecture concludes by highlighting the deeper significance of the log transform. It not only helps in data transformation but also reflects patterns in nature and human perception. Sound is perceived logarithmically, which is why the decibel scale is used. Similarly, the human experience of wealth follows a logarithmic pattern: losing or gaining a fixed amount of money has very different utility depending on overall wealth. Thus, the log transform is both mathematically useful and naturally fundamental.

**G) Power, Log, and Box-Cox Transformations in Code**

OK, so in this lecture, we are going to investigate the Box Cox and other Time series transformations in code.

We’ll start by downloading a famous time series dataset called Airline Passengers. Next, we’re going to import the libraries — Numpy, Pandas, Matplotlib, and also the BoxCox function from Scipy. So the code is:
"import numpy as np; import pandas as pd; import matplotlib.pyplot as plt; from scipy.stats import boxcox"

Next, we’re going to read in the CSV file using Pandas. "df = pd.read_csv('AirPassengers.csv', parse_dates=['Month'], index_col='Month')"

Now, one thing I always like to do whenever I load in some data is to just see what it looks like. This makes me more confident that my code is working as expected. So we can check the first few rows by writing "print(df.head())".

OK, so we can see that for the index, we have the date, which is monthly, and we have one integer column called passengers.

The next step is to plot our dataset just to see what we’re dealing with. "df['Passengers'].plot(figsize=(12,6), title='Airline Passengers'); plt.show()".

Now, there are several characteristics of this data I want you to notice. Number one, it has a trend — this time series is going upward to the right. Number two, it has seasonality — there is a repeating pattern in time. Number three, the amplitude of this seasonal pattern increases over time.

The next step will be to try a square root transform. We can do this by writing "df['sqrt_passengers'] = np.sqrt(df['Passengers'])".

Now let’s plot this transformed column: "df['sqrt_passengers'].plot(figsize=(12,6), title='Square Root Transform'); plt.show()".

We can see that the time series has been squashed down slightly, but the amplitude of the seasonal pattern still seems to increase over time.

The next step is to try the log transform. "df['log_passengers'] = np.log(df['Passengers'])".

Let’s plot this new column: "df['log_passengers'].plot(figsize=(12,6), title='Log Transform'); plt.show()".

This log transform seems to do a pretty good job at squashing down the data to make it look more uniform over time.

The final step will be to do a BoxCox transform. This function takes in a one-dimensional dataset as input and returns the transformed data along with the optimal value of lambda. "df['boxcox_passengers'], lam = boxcox(df['Passengers'])".

Let’s print out the lambda: "print('Optimal lambda:', lam)".

For this dataset, we get about 0.15, which is kind of in between the log transform and the square root transform.

Now let’s plot the BoxCox transformed data: "pd.Series(df['boxcox_passengers'], index=df.index).plot(figsize=(12,6), title='BoxCox Transform'); plt.show()".

OK, and we see that it definitely looks like something in between the square root and the log transforms.

The next step is to visualize our data in the form of a histogram. For the raw passenger data, "df['Passengers'].hist(bins=30); plt.title('Raw Passengers'); plt.show()". For the square root data, "df['sqrt_passengers'].hist(bins=30); plt.title('Square Root'); plt.show()". For the log data, "df['log_passengers'].hist(bins=30); plt.title('Log Transform'); plt.show()". And for the BoxCox data, "pd.Series(df['boxcox_passengers']).hist(bins=30); plt.title('BoxCox Transform'); plt.show()".

From these histograms, we can observe that the raw data is concentrated at the lower values, the square root has flattened things out a little, the log looks more symmetric, and the BoxCox transform produces a shape closer to a normal distribution.

And that’s pretty much it for this code walkthrough. These transformations help us deal with variance and growth patterns in time series, and even though we won’t always use BoxCox in practice, it’s a useful tool to be aware of.

**Notes:**

In this lecture, we investigate the Box-Cox and other time series transformations in code. We start by downloading a famous time series dataset called Airline Passengers. Next, we import the libraries — Numpy, Pandas, Matplotlib, and also the BoxCox function from Scipy. The code is:
import numpy as np; import pandas as pd; import matplotlib.pyplot as plt; from scipy.stats import boxcox.

We then read in the CSV file using Pandas:
df = pd.read_csv('AirPassengers.csv', parse_dates=['Month'], index_col='Month').

After loading the data, it is always useful to inspect the first few rows to gain confidence that the code is working as expected. This can be done by writing print(df.head()). The output shows that for the index, we have the date (monthly), and there is one integer column called passengers.

The next step is plotting the dataset to visualize its characteristics:
df['Passengers'].plot(figsize=(12,6), title='Airline Passengers'); plt.show().

From this plot, we notice three key aspects: (1) there is a trend, as the time series is going upward to the right, (2) there is seasonality, indicated by a repeating pattern over time, and (3) the amplitude of the seasonal pattern increases over time.

The first transformation to try is the square root transform:
df['sqrt_passengers'] = np.sqrt(df['Passengers']).
We then plot the transformed column using:
df['sqrt_passengers'].plot(figsize=(12,6), title='Square Root Transform'); plt.show().

This squashes the data down slightly, but the amplitude of the seasonal pattern still increases over time.

Next, we apply the log transform:
df['log_passengers'] = np.log(df['Passengers']).
The transformed column can be plotted with:
df['log_passengers'].plot(figsize=(12,6), title='Log Transform'); plt.show().

This log transform does a good job at squashing the data, making it appear more uniform across time.

The final transformation is the BoxCox transform. This function requires a one-dimensional dataset as input and returns the transformed data along with the optimal lambda value. We apply it as follows:
df['boxcox_passengers'], lam = boxcox(df['Passengers']).
We print the lambda using:
print('Optimal lambda:', lam).

For this dataset, the optimal lambda is about 0.15, which lies between the log transform and the square root transform. The transformed data can be plotted using:
pd.Series(df['boxcox_passengers'], index=df.index).plot(figsize=(12,6), title='BoxCox Transform'); plt.show().

The plot confirms that the BoxCox transform looks like something in between the square root and the log transforms.

The next step is visualizing the data distributions with histograms. For raw passengers:
df['Passengers'].hist(bins=30); plt.title('Raw Passengers'); plt.show().
For the square root:
df['sqrt_passengers'].hist(bins=30); plt.title('Square Root'); plt.show().
For the log:
df['log_passengers'].hist(bins=30); plt.title('Log Transform'); plt.show().
And for the BoxCox:
pd.Series(df['boxcox_passengers']).hist(bins=30); plt.title('BoxCox Transform'); plt.show().

From these histograms, we observe that the raw data is concentrated at the lower values, the square root has flattened things slightly, the log transform makes the data more symmetric, and the BoxCox transform produces a distribution closer to normal.

In conclusion, this code walkthrough shows how transformations such as square root, log, and BoxCox help deal with variance and growth patterns in time series. Even though BoxCox is not always used in practice, it is a powerful tool worth being aware of.

**Summary:**

This lecture demonstrated how to apply and visualize transformations on the Airline Passengers dataset. After loading the data using Pandas and inspecting its structure, we plotted the series and identified key features such as trend, seasonality, and increasing amplitude. We then applied three transformations — square root, log, and BoxCox. The square root slightly reduced the growth, but the seasonal amplitude remained. The log transform performed well in compressing the data and making it appear more uniform over time. The BoxCox transform, which automatically finds an optimal lambda (around 0.15 in this case), produced results between the square root and log transforms. Finally, histograms showed how each transformation reshaped the data distribution, with BoxCox producing something close to normal. Overall, these transformations are useful for handling variance and growth in time series, and BoxCox, though not always used in practice, is an important technique to understand.

**H) Forecasting Metrics**

So in this lecture, we are going to discuss error metrics commonly used in Time series analysis.

Now, because time series forecasting is essentially a regression task, these error metrics are the same as what you’ve likely encountered before in regression.

One metric that shows up very often in statistics, machine learning, deep learning, and engineering is the Sum of Squared Errors (SSE). Suppose we have n predictions, so we have 𝑦𝑖yi going from 1 up to 𝑛 n. For the SSE, we simply take the difference between each 𝑦 𝑖 y i and 𝑦^𝑖y^	i, square that difference, and add all the squared differences together. In Python:
"sse = np.sum((y_true - y_pred) ** 2)"

The reason we square these differences is because sometimes the prediction may be less than the target, and other times the target may be less than the prediction. Since we don’t want errors to cancel each other, squaring ensures they’re always non-negative.

A bonus to using squared error is that it coincides with maximizing the Gaussian likelihood — that is, it’s the “correct” error metric to minimize when errors are normally distributed.

However, one downside to the SSE is that it depends on the number of data points you have. If you have 100 predictions vs. 1,000 predictions, your SSE will naturally be larger in the second case simply because there are more terms.

So instead, we often use the Mean Squared Error (MSE), which simply divides by the number of samples:
"mse = np.mean((y_true - y_pred) ** 2)"

This makes the metric invariant to the number of samples. In fact, this serves as an estimate of the expected squared error, which is what many algorithms are designed to minimize.

But there’s another issue: the units. If you’re forecasting temperature in Kelvin, the MSE is in Kelvin squared — which is unintuitive. So we often take the square root, giving the Root Mean Squared Error (RMSE):
"rmse = np.sqrt(mse)"

The advantage is that RMSE is on the same scale as the original data, making it much easier to interpret. For example, if you’re predicting house prices, saying “RMSE = 100 dollars” makes more sense than “MSE = 10,000 square dollars.”

Now, you might wonder: why work with squared errors at all? Why not just take the absolute value? That brings us to the Mean Absolute Error (MAE):
"mae = np.mean(np.abs(y_true - y_pred))"

This is very intuitive: it’s directly on the same scale as the data, and it also has a probabilistic interpretation. Whereas squared error relates to a Gaussian likelihood, absolute error relates to a Laplace likelihood. Importantly, minimizing MAE makes your model less sensitive to outliers, which can be beneficial in practice.

Interestingly, many practitioners train their models using squared error but report absolute error as a metric. With libraries like scikit-learn, "from sklearn.metrics import mean_absolute_error; mae = mean_absolute_error(y_true, y_pred)", you can compute this easily.

But here’s the catch: both MSE and MAE depend on the scale of the data. Predicting house prices (in millions of dollars) vs. predicting stock returns (fractions of a percent) gives you errors on very different scales. Comparing across tasks is not straightforward.

This is where scale-invariant metrics come in, the most common of which is R-squared. Unlike error metrics, here higher is better. It can be computed as:
"from sklearn.metrics import r2_score; r2 = r2_score(y_true, y_pred)"

Conceptually, R² compares your model’s performance to simply predicting the mean of the targets. Perfect predictions give R² = 1. A model that does no better than predicting the mean gives R² = 0. And yes, it’s possible to get negative R² if your model is worse than just predicting the mean.

Now let’s move to percentage-based errors. The Mean Absolute Percentage Error (MAPE) is useful when you want to express error in relative terms:
"mape = np.mean(np.abs((y_true - y_pred) / y_true)) * 100"

For example, if the true house price is $1,000,000 and you predict $1,001,000, that’s only a 0.1% error — which is tiny. But if the true price is $1,000 and you’re off by the same $1,000, that’s a 100% error — which is huge.

However, MAPE has problems: it’s not symmetric, and when the denominator is zero, the error explodes to infinity. To fix the asymmetry, people use the Symmetric MAPE (sMAPE):
"smape = np.mean(2 * np.abs(y_pred - y_true) / (np.abs(y_true) + np.abs(y_pred))) * 100"

This version averages the true and predicted values in the denominator, making the metric symmetric.

So, to summarize:

"sse = np.sum((y_true - y_pred) ** 2)" → depends on sample size.

"mse = np.mean((y_true - y_pred) ** 2)" → scale-sensitive, in squared units.

"rmse = np.sqrt(mse)" → same units as data.

"mae = np.mean(np.abs(y_true - y_pred))" → robust to outliers.

"r2_score(y_true, y_pred)" → scale-invariant goodness-of-fit.

"mape" and "smape" → percentage-based, intuitive for relative error.

Again, we won’t use all of these every time, but the purpose here is to make you aware of these tools. Different papers and professionals prefer different metrics, and having this shared language is key when working in the field.

**Notes:**

In this lecture, we discuss error metrics commonly used in time series analysis. Since time series forecasting is essentially a regression task, the error metrics are the same as those encountered in regression.

One commonly used metric is the Sum of Squared Errors (SSE). Suppose we have n predictions, with 
𝑦 𝑖 y i going from 1 up to n. For the SSE, we take the difference between each 𝑦𝑖yi and 𝑦𝑖^yi^, square that difference, and add all the squared differences together. In Python:

sse = np.sum((y_true - y_pred) ** 2)

The squaring ensures that errors do not cancel each other out and are always non-negative. Another advantage of squared error is that it coincides with maximizing the Gaussian likelihood, making it the correct error metric to minimize when errors are normally distributed. A downside of SSE is that it depends on the number of data points, so more predictions naturally produce a larger SSE.

To address this, we use the Mean Squared Error (MSE), which divides SSE by the number of samples:

mse = np.mean((y_true - y_pred) ** 2)

This makes the metric independent of the sample size and serves as an estimate of the expected squared error, which many algorithms are designed to minimize. However, the units of MSE are squared, which can be unintuitive. To fix this, we use the Root Mean Squared Error (RMSE):

rmse = np.sqrt(mse)

This has the advantage of being on the same scale as the original data, making interpretation easier. For example, in predicting house prices, saying RMSE = 100 dollars is clearer than MSE = 10,000 square dollars.

Another approach is to use absolute values instead of squared errors, leading to the Mean Absolute Error (MAE):

mae = np.mean(np.abs(y_true - y_pred))

This metric is intuitive, lies on the same scale as the data, and has a probabilistic interpretation. Whereas squared error corresponds to a Gaussian likelihood, absolute error corresponds to a Laplace likelihood. Importantly, minimizing MAE makes the model less sensitive to outliers. Many practitioners train using squared error but report absolute error. With scikit-learn, MAE can be computed using:

from sklearn.metrics import mean_absolute_error
mae = mean_absolute_error(y_true, y_pred)

Both MSE and MAE depend on the scale of the data, making cross-task comparisons difficult. This is where scale-invariant metrics like R-squared are useful. R² is computed as:

from sklearn.metrics import r2_score
r2 = r2_score(y_true, y_pred)

Conceptually, R² compares model performance to predicting the mean of the targets. Perfect predictions yield R² = 1, while always predicting the mean yields R² = 0. Negative R² indicates worse performance than predicting the mean.

Percentage-based metrics are also important. The Mean Absolute Percentage Error (MAPE) expresses error in relative terms:

mape = np.mean(np.abs((y_true - y_pred) / y_true)) * 100

This is intuitive, but has problems such as asymmetry and exploding values when the denominator is zero. To address asymmetry, the Symmetric MAPE (sMAPE) is used:

smape = np.mean(2 * np.abs(y_pred - y_true) / (np.abs(y_true) + np.abs(y_pred))) * 100

This averages the true and predicted values in the denominator, making the metric symmetric.

To summarize:

SSE depends on sample size.

MSE is scale-sensitive and in squared units.

RMSE is in the same units as the data.

MAE is robust to outliers.

R² is scale-invariant and measures goodness-of-fit.

MAPE and sMAPE are percentage-based and intuitive for relative error.

Not all metrics are used every time, but awareness of these tools is essential, since different papers and professionals prefer different metrics. Having this shared language is key in the field.

**Summary:**

This lecture introduced error metrics commonly used in time series forecasting, which are the same as regression metrics. SSE sums squared errors but depends on sample size. MSE resolves this by averaging, though its squared units are unintuitive. RMSE takes the square root, restoring the original scale and improving interpretability. MAE uses absolute errors, making it intuitive, less sensitive to outliers, and connected to the Laplace likelihood. However, both MSE and MAE are scale-dependent. To address this, R² provides a scale-invariant measure, comparing performance against predicting the mean, with values ranging from 1 (perfect) to negative values (worse than mean). For relative errors, MAPE expresses errors in percentage terms but suffers from asymmetry and division by zero. sMAPE improves on this by symmetrizing the denominator. Overall, these metrics—SSE, MSE, RMSE, MAE, R², MAPE, and sMAPE—equip practitioners with a toolkit for evaluating forecasts, each suited to different contexts.

**I) Financial Time Series Primer**

One of the most popular applications of time series analysis isn't finance, although this is not the only application of time series, it's one that I know a lot of you are thinking about now. Unfortunately, a lot, of course, is out there. Simply taking the price of a stock and treating that like any other time series seems completely reasonable. What's the difference between one time series and another? Well, in this course you're going to learn that there's actually a huge difference. None of this is obvious at first, but I hope that throughout this course you will build your skill to a level necessary to understand what I'm saying.

You might start this course with a naive perspective, but by the end of this course, this perspective will mature. If your logic right now is Lithium's plus stock price prediction equals profit, then I would consider you as someone who falls into this naive category. Now, don't consider this to be a bad thing, but a good thing. You are going to get the most out of this course.

So this lecture is a financial time series primer. There are certain operations and definitions you simply have to know about when you're dealing with stock price data. Now, although I've taught financial engineering elsewhere very in depth, you can think of this lecture as like a summary of those concepts.

OK, so clearly the stock price over time is an example of a time series. It's continuous, valued, and it can be thought of as discrete time. For example, when you download stock price data from Yahoo Finance, you might get daily data or hourly data in regularly spaced intervals. In more advanced courses, you can think of stock prices as continuous time, although, as mentioned, that would be a separate course.

Now, in practice, what we are interested in is not the stock price, but rather the stock return. Let's think about the intuition behind this. We learned earlier that when we talk about forecasting metrics, it's nice when they are scale invariant. If your guess for the price of a one million dollar house is off by one thousand, that's not so bad. But if your guess for the price of a five dollar coffee is off by five dollars, that's a pretty bad guess. So it's more natural to think in terms of percentages. The percent change tells us how much money we've made or lost on a stock that we own. We call this the stock return. The equation is very simple. And of course, you've seen this before. It's the final price minus the initial price divided by the initial price: "return = (final_price - initial_price) / initial_price".

Now, in practice, because we index our prices by time measured in periodic intervals, it's common to consider the return for each of those periods also indexed by time. So we say our return at time t is equal to the price at time t minus the price at time t-1, divided by the price at time t-1: "return[t] = (price[t] - price[t-1]) / price[t-1]". Note that this is also equal to "return[t] = (price[t] / price[t-1]) - 1". And also note that we sometimes call this the net return, although I usually won't make this distinction.

**Notes:**

One of the most popular applications of time series analysis is finance. Although this is not the only application of time series, it is one that comes to mind very often. Simply taking the price of a stock and treating it like any other time series might seem completely reasonable at first. However, there is actually a huge difference between one kind of time series and another. This difference is not obvious initially, but the purpose of this course is to build the necessary skills to understand these differences.

Students may begin the course with a naive perspective, such as thinking “lithium’s plus stock price prediction equals profit.” This naive view is not considered bad, but rather a starting point that allows one to get the most out of the course, because by the end of it this perspective will mature into a more sophisticated understanding.

This lecture serves as a financial time series primer. There are certain operations and definitions that one must know when working with stock price data. While financial engineering can be taught in great depth, this lecture is positioned as a summary of the essential concepts.

Stock price over time is itself an example of a time series. It is continuous-valued and can be thought of in discrete time form. For example, when downloading stock price data from Yahoo Finance, the data might come as daily or hourly values at regularly spaced intervals. In more advanced courses, stock prices may be treated in continuous time, though that is a different subject entirely.

In practice, what we are really interested in is not the stock price itself, but the stock return. The intuition behind this is tied to the idea of scale invariance in forecasting metrics. For instance, being off by $1,000 in estimating the price of a one million dollar house is not a large error, but being off by $5 in estimating the price of a $5 coffee is a very large error. Thus, percentage changes provide a more natural and useful way to measure outcomes. This percentage change is called the stock return, and it tells us how much money has been made or lost on a stock.

The formula for return is simple and familiar:
return = (final_price - initial_price) / initial_price.

Since prices are indexed by time in periodic intervals, it is common to define return for each interval as well. At time t, the return is:
return[t] = (price[t] - price[t-1]) / price[t-1].

This can also be expressed as:
return[t] = (price[t] / price[t-1]) - 1.

Sometimes this is referred to as the net return, though this distinction is not always emphasized.

**Summary:**

This lecture introduces financial time series as one of the most popular applications of time series analysis. While stock prices may at first appear to be just another time series, they have unique characteristics that require special treatment. Beginners often approach the topic with a naive view, such as assuming simple stock prediction will lead directly to profit, but the course aims to develop a more mature understanding.

The lecture highlights that stock prices over time form a time series, usually viewed in discrete time with regularly spaced intervals like daily or hourly data. However, what matters more in practice is not the price itself but the return, which reflects percentage changes and therefore accounts for scale differences. This makes returns more natural for analysis than raw prices.

The return is defined as the change in price relative to the initial price. Over time, it is calculated at each interval using the formula (price[t] - price[t-1]) / price[t-1], or equivalently, (price[t] / price[t-1]) - 1. This measure, sometimes called net return, is central to analyzing financial time series.

**J) Price Simulations in Code**

In this lecture, you're going to look at a simple example of how to simulate stock prices, assuming that the log returns come from a normal distribution.

Now, this might seem at first to be a strange exercise, but it should get you thinking. We'll see how totally unpredictable randomness can lead to something that looks very much like a stock race time series. In fact, this exact method can be used for doing Montecarlo simulations and evaluating the Black-Scholes formula. Furthermore, it is also useful for when we want to analyze certain rules of thumb for Arima. This may not make too much sense right now, but you'll see how this kind of approach can help to validate some of the rules that we use for a rhema model selection.

OK, so let's start by importing nonpaying matplotlib. "import numpy as np; import matplotlib.pyplot as plt"

The next step is to set a few constants will be using, such as the number of time steps, the initial price and the drift term. "T = 40; P0 = 100; drift = 0.001"

The next step is to run our simulation, so we'll start by taking the log of the price and setting it to last P last P is a variable will continue to update throughout the loop, since the current price will always depend on the last price. "lastP = np.log(P0)"

The next step is to create two arrays, to store log returns and our prices, and of course, these should both have length T. "log_returns = np.zeros(T); prices = np.zeros(T)"

The next step is to enter a loop that goes 40 iterations inside the loop. We'll start by sampling a random log return from a zero mean normal distribution with standard deviation zero point zero one. "for t in range(T): r = np.random.normal(0, 0.01)"

The next step is to compute our new log price. This is equal to the old log price, plus the drifter, plus the random noise. "lastP = lastP + drift + r"

The next step is to store the log return and the new price note that we don't actually make use of the log returns, but you may find them to be useful in later code for the price. Note that we have to take the exponential since we want to plot the price and not the log price. "log_returns[t] = r; prices[t] = np.exp(lastP)"

The final step in this loop is to assign P to last P so that last P has the correct value in the next iteration. "pass"

OK, and so in the next block, we are going to plot our simulated time series. "plt.plot(prices); plt.title('Simulated Stock Price'); plt.show()"

So as you can see, this certainly looks like a plausible stock price evolution. In the coming lectures, you learn about the why behind what we just did. And hopefully this will give you some insight behind this exercise.

**Notes:**

In this lecture, the focus is on simulating stock prices using the assumption that the log returns come from a normal distribution. At first, this might appear to be a strange exercise, but the purpose is to show how unpredictable randomness can generate something that looks very much like a realistic stock price time series. This approach is widely used for Monte Carlo simulations, evaluating the Black-Scholes formula, and even validating rules of thumb in ARIMA model selection.

The first step is to import the required libraries: "import numpy as np; import matplotlib.pyplot as plt".

Next, a few constants are defined for the simulation. These include the number of time steps, the initial price, and the drift term: "T = 40; P0 = 100; drift = 0.001".

The simulation begins by taking the logarithm of the initial stock price and assigning it to a variable called lastP, which will be continuously updated during the loop: "lastP = np.log(P0)".

Two arrays are then created to store the log returns and the simulated prices, each with length T: "log_returns = np.zeros(T); prices = np.zeros(T)".

A loop is then run for T iterations. Inside the loop, a random log return is sampled from a normal distribution with mean 0 and standard deviation 0.01: "for t in range(T): r = np.random.normal(0, 0.01)".

The new log price is then computed by updating the old log price with the drift term and the sampled random noise: "lastP = lastP + drift + r".

After that, the log return is stored in the log_returns array, and the actual stock price is computed by exponentiating the log price. This price is then stored in the prices array: "log_returns[t] = r; prices[t] = np.exp(lastP)".

At the end of each iteration, lastP is updated to ensure it has the correct value for the next iteration: "pass".

Finally, the simulated stock price path is plotted to visualize the results: "plt.plot(prices); plt.title('Simulated Stock Price'); plt.show()".

The resulting plot resembles a plausible stock price trajectory, even though it was created purely from randomness and a drift term. The lecture concludes by noting that in upcoming lessons, the underlying logic and significance of this simulation will be explained further, providing insight into why this technique is valuable for financial modeling.

**Summary:**

This lecture explains how to simulate stock prices by assuming that log returns follow a normal distribution. The exercise demonstrates how random variation combined with a drift term can produce a time series resembling real stock prices. This method is useful for Monte Carlo simulations, Black-Scholes evaluation, and ARIMA model validation.

The process begins with importing NumPy and Matplotlib, setting constants, and working with log prices. A loop is used to sample random log returns, update log prices, compute actual prices, and store the values. Finally, the simulated stock price series is plotted, showing a realistic price evolution. While simple, this method forms the basis for more advanced financial time series modeling.

**K) Random Walks and the Random Walk Hypothesis**

So in this lecture, we are going to discuss a very important topic when it comes to Financial Times series, this is the random walk in the corresponding random walk hypothesis. To give you a very brief summary, a random walk is what we implemented when we did price simulations. This lecture will expand on what we did by taking a more theoretical look at what we've already done in practice. The practical part is useful, but the theoretical part is critical for providing you with necessary insights. In fact, we'll learn later in this course that the random walk is a special case of an Arima, a very important time series model.

So what is the random hypothesis? Well, put simply, it says that stock prices follow a random walk. Now, of course, you may not know exactly what a random walk is yet, but that's what this lecture is about. Now because of the nature of random walks, if stock prices do, in fact, follow a random walk, then they are unpredictable. The rest of this lecture will show you how.

But first, let's discuss some of the history behind the random walk hypothesis. Firstly, the mathematical concept of random walks has existed for a long time. As you'll see, it's just a Markov process. And so it's something you would normally learn in probability class. The random walk hypothesis is specific to finance and stock prices in particular. It was popularized in the 70s when a book called A Random Walk Down Wall Street was released. In fact, this was the book that also popularized the efficient market hypothesis. Note that both the random walk hypothesis and the efficient market hypothesis lead to the same conclusion, which is that you can't beat the market.

Now, of course, there are people who don't believe in the random hypothesis. And so another book has come out called A Non Random Walk Down Wall Street. Interestingly, this book came out almost 30 years later after A Random Walk Down Wall Street. So it's not as if the random hypothesis and the efficient market hypothesis are ideas which are easily debunked. In this course, we're actually going to fit models to stock prices and we'll find that sometimes the best fitting model is, in fact, a random walk.

So what is a random walk? Well, probably the simplest random walk works like this: start at any price. Then in order to generate the next price, simply pick either plus one or minus one with equal probability. So P one is equal to P0 plus E one where E one can be either minus one or plus one, then generate P two from P one in the same way by picking either plus one or minus one with equal probability and then adding it to P1. Then we find P three and then we find P four and so on. So this is a random walk. Basically, you can imagine yourself walking on the sidewalk in one dimension. At every step, you either decide to take one step to the left or one step to the right based on the result of a coin flip. Your walk is then a random walk.

Notice one important property of the random walk. It's impossible to predict the next value. You only have a 50 percent chance of getting it right. In other words, your ability to predict the result of your walk is the same as your ability to predict the result of a series of coin flips.

Now, we know that changes in stock price aren't just minus one and plus one, but can be real-valued. In fact, we spent a lot of time in the previous section of this course trying to figure out what is the distribution that stock returns follow. Let's assume for now that the noise term is Gaussian. What would our algorithm be for generating stock prices? Again, we start at P0 equal to some arbitrary value. To find the next price, we first sample E from our Gaussian, then we add P zero plus one to find P one, the next price. We do the same thing to generate P2 and P3 and so forth. This should sound familiar because it's exactly what we did in our price simulation exercise from the previous lecture. In fact, that was exactly a random walk.

Notice again how we can't predict P one from P zero, or equivalently, we can't predict P one minus P zero, which is just E one, which is Gaussian noise. We can only predict one insofar as we know its expected value. Here's something interesting we can do that helps us understand why working with log prices is valuable. The general formula for a random walk with a drift is as follows. μ is called the drift term, and it's considered to be constant. If you're thinking of a time series, this would control the trend of the Time series. E of T is a Gaussian with mean zero and some variance σ². In this case, time T and time T minus one are the log prices at time T and time T minus one respectively. Note that if I take time T minus one to the left-hand side, I get a time T minus time T minus one, which is the log return. If we were working with non-log returns, this wouldn't be as convenient, since we would need a P of T minus one in the denominator to represent the return. What this says is that the log return is just the thing on the right-hand side, which is just the Gaussian with mean zero and variance σ².

So the random walk model goes hand in hand with log prices and log returns. In fact, this model is the basis for the Black-Scholes formula which earned the Nobel Prize in economics. Now, the big question is, of course, is the random walk hypothesis correct? Well, let's recognize that there are some hidden assumptions in the random walk model. First is that the log returns are i.i.d.—independent and identically distributed. We have seen that this may not be true because we have observed volatility clustering. If the volatility changes over time, then by definition it's not identically distributed. Furthermore, if the volatility in one period has some relationship to nearby periods, that is high. Volatility is clustered with other high volatility, then it's also not independent.

At the same time, the random walk model is convenient and easy to work with. We will find that when we fit Arima models to stock prices, sometimes the best fitting model will be a random walk. So it wouldn't be wrong to say that sometimes, for certain periods of time, stock prices do look like they follow a random walk. As with the efficient market hypothesis, it's possible to use statistical tests to determine whether or not stock prices follow a random walk.

Now, since this is, of course, on Time series, we're going to do some time series analysis on random walks. Let's recognize that a random walk is just a specific instance of a Markov chain. If you've ever taken any of my courses on NLP or reinforcement learning, you should be familiar with this concept. The basic idea is this. Consider the sentence: “The quick brown fox jumps over the lazy dog.” If I gave you the sequence, “The quick brown fox jumps over the lazy,” how can you predict the next word of this sentence? Well, one solution is to build a probability distribution so you have the probability of the word at time t given the word at time T minus one, given the word at time T minus two, and so on. We call such a model a language model.

Well, to get to the point, the Markov assumption says this: it says that instead of the word at time t depending on all previous words, it only depends on the most immediate preceding word. That is, P(word at time T | word at time T-1, word at time T-2, …) = P(word at time T | word at time T-1).

Now you might think, OK, that's fine, but let's make this a little less abstract. Suppose I give you the word “lazy” and I ask you to predict the next word in my sentence. Of course, there are many possibilities. It could be “lazy dog,” but you'd probably be cheating because that's the sentence I gave you earlier. It might be “lazy programmer,” who is the author of this course, but again, you're going to use exogenous data to make your prediction. How about “lazy student”? In fact, it's quite difficult to know with any certainty exactly what the next word will be, given only a single word. Consider the word. The next word could be practically anything. So the lesson here is that the Markov assumption is an extremely strong modeling assumption. At the same time, it's quite useful.

So let's assume we have a Gaussian random walk. "X[t] = X[t-1] + F[t]" OK, this is excessive. T equals X of T minus one plus F.T. Where F.T. is Gaussian distributed with mean zero and variance σ². In this case, we can see that X of T is completely determined by a Gaussian distribution centered at X of T minus one with a variance σ². That is, it does not depend on any previous values in the series, not X of T-2, not X of T-3, and so on. Therefore, the Gaussian random walk forms a Markov chain.

So if stock prices follow a Gaussian random walk, then the next obvious question is how do we forecast? Remember that because the next step is essentially random, the best we can do is find the expected value. Well, the expected value of a Gaussian with mean X of T-1 is just X of T-1. So what does this say? It's saying that if your stock price follows a random walk, then your best guess for the next stock price in the series is just the previous value. We cannot do any better than this. Notice that this justifies our method of filling in missing data, which is to copy the previous stock price forward in time.

Now, as you know, often when we make estimates and statistics, we also want to quantify how confident we are in those estimates. Let's suppose we start at X of T and we want to forecast τ steps into the future to find X of T+τ. How? We already know the expected value of X[T+τ] is just X of T, the same value we started with. But what about the variance? Well, we can use our price simulation formula. We know that X[T+1] = X[T] + F[T+1]. Based on that, we also know that X[T+2] = X[T+1] + F[T+2], which is added one to all the time indices. However, we can substitute X[T+1] and then we would get X[T] + F[T+1] + F[T+2], and then we keep following this pattern until we get to T+τ. So X[T+τ] = X[T] + F[T+1] + F[T+2] + … + F[T+τ].

Now luckily we did something exactly like this in the previous section. If all the F’s are Gaussian with mean zero and variance σ², then their sum has mean zero and variance τσ². Therefore, we can say that the variance in our estimate increases linearly with τ. More commonly we work with the standard deviation, so we can see that the standard deviation of our forecast increases with the square root of the number of forecasting steps.

Let's consider a well-known theorem from statistics, the Central Limit Theorem. We know that our forecast, the time T+τ, is the last known price of T plus the sum of a bunch of noise terms. Recall that the Central Limit Theorem says that this sum tends to a Gaussian distribution. And so even if your returns do not necessarily follow a Gaussian distribution in the short term, what happens in the long term? Well, in the long term, you're just adding up a bunch of random variables. And due to the Central Limit Theorem, their distribution approaches a Gaussian.

I want to end this lecture with a tale about a famous experiment run by The Wall Street Journal in 1988. And this experiment, called the Dart Throwing Investment Contest, had professional stock traders from the New York Stock Exchange compete against dummy investors who simply threw darts on a board to choose stocks randomly. Now, granted, one might argue that throwing darts is not actually random and there may have been better ways to make random choices. In any case, they found that professional investors beat the dummy investors sixty-one out of one hundred times, and the dummy investors won only 39 out of 100 times.

So you might think it's better to go with a professional investor rather than just picking stocks randomly. However, the professional investors only beat the market 51 out of 100 times. This is why it's often advised not to use active investing, although your bank will tell you otherwise. Just don't forget your bank is there to sell you things, not to give you good advice if you buy into an actively managed fund. First of all, you may only have a 50 percent chance of beating the market and on average you will match the market. However, the fees for actively managed funds are much higher than passively managed funds. Therefore, if you invest in the market itself, your fees will be much lower and you will have the same expected return anyway.

**Notes:**

In this lecture, we discuss random walks and the random walk hypothesis, which are central to financial time series analysis. Recall from the previous lecture’s price simulation exercise that a random walk is what we implemented when simulating stock prices. This lecture expands on that by providing the theoretical background, which is crucial for understanding why stock prices behave the way they do and how this connects to ARIMA models.

The random walk hypothesis states that stock prices follow a random walk and are therefore unpredictable. Historically, the concept of random walks predates finance and comes from probability theory. In finance, it was popularized by the 1973 book A Random Walk Down Wall Street, which also popularized the efficient market hypothesis. Both hypotheses imply that consistently beating the market is impossible.

A simple random walk can be described as: start at an initial price P0. The next price is given by P1 = P0 + E1, where E1 is either +1 or -1 with equal probability. The subsequent price P2 = P1 + E2 follows the same logic, and so on. This is equivalent to walking on a line and flipping a coin to decide your next step. The important property is that the next step is completely unpredictable: the probability of guessing correctly is 50%, just like a coin flip.

In reality, stock price changes are real-valued. If we assume Gaussian noise, then the next price is generated as P[t] = P[t-1] + E[t], where E[t] ~ Gaussian(0, σ²). This is exactly what was done in the price simulation exercise in the previous lecture. Using log prices and log returns is convenient because the log return is simply log(P[t]) - log(P[t-1]) = E[t], which is Gaussian. Including a drift term, μ, the random walk with drift becomes log(P[t]) = log(P[t-1]) + μ + E[t], where E[t] is Gaussian noise. This model forms the basis of the Black-Scholes formula.

However, there are assumptions in this model:

i.i.d. log returns: they must be independent and identically distributed. This may fail in practice due to volatility clustering.

Despite the limitations, random walk models are convenient and sometimes the best-fitting model for stock prices in certain periods.

Mathematically, a Gaussian random walk is a Markov chain: "X[t] = X[t-1] + F[t]", where F[t] ~ Gaussian(0, σ²). Here, the next state only depends on the current state, not on any previous states: X[t-1], X[t-2], ….

Forecasting a random walk is straightforward: the best estimate for the next value is simply the previous value: "X[t+1]_forecast = X[t]". The variance of a forecast τ steps ahead grows linearly: "Var(X[T+τ]) = τσ²", so the standard deviation grows with the square root of τ: "Std(X[T+τ]) = sqrt(τ) * σ".

By the Central Limit Theorem, even if short-term returns are not Gaussian, summing many random variables (noise terms) produces a Gaussian distribution in the long run.

A famous experiment by the Wall Street Journal (1988), the Dart Throwing Investment Contest, showed that randomly picking stocks often performs nearly as well as professional investors. Professionals beat random picks only slightly more than 50% of the time, highlighting the difficulty of consistently outperforming the market. This supports the idea of passive investing, as fees for active management reduce expected returns.

**Summary:**

In this lecture, we explored the random walk hypothesis, which is central to understanding financial time series. A random walk describes a process where the next value in a series, such as a stock price, depends only on the current value plus a random noise term. This makes the series inherently unpredictable, as the best guess for the next value is simply the current value. In practice, stock prices are often modeled using Gaussian random walks, where the noise term follows a normal distribution with mean zero and some variance. This forms a Markov chain, meaning that each new price depends only on the previous price and not on any earlier history.

We also discussed the importance of log prices and log returns, as these simplify modeling and make the random walk framework more convenient. Log returns are just the differences of log prices, which under the random walk model are Gaussian with mean zero. Adding a drift term allows the model to capture an overall trend in the time series. This model underpins important financial theories and formulas, including the Black-Scholes formula.

Forecasting in a random walk context is limited: the expected value of the next step is always equal to the current value, and the variance of forecasts increases linearly with the number of steps ahead. Over longer horizons, the Central Limit Theorem ensures that the sum of random noise terms converges to a Gaussian distribution, even if short-term returns are not perfectly normal.

Finally, practical experiments, such as the 1988 Dart Throwing Investment Contest, illustrate that even professional investors often fail to consistently beat the market, highlighting the relevance of passive investing. The random walk model provides both a theoretical foundation and a practical explanation for why stock prices are difficult to predict, while also serving as a building block for more advanced time series models like ARIMA.

**L) The Naive Forecast and the Importance of Baselines**

In this lecture, we are going to discuss a method of forecasting called the naive forecast. Before we discuss what the naive forecast is, let's talk about the importance of establishing baselines in machine learning. The purpose of a baseline is to have a relevant point of comparison.

To give you an example, suppose that you went to your professor tomorrow and say, “Hey, I just made a great discovery. I built a model using deep learning and I got 99 percent accuracy.” Unfortunately, the statement is meaningless because you don't have a context of a baseline. Your professor might say, “But student, we already know that a simple linear model achieves 100 percent accuracy.” In this case, your model is worse than what currently exists. And furthermore, it's also slower.

So how can we make sure that we don't make this mistake? The answer is using a baseline. You'll notice that when you're reading machine learning papers, they often compare their results against the existing state of the art. Now, it's important to realize that you don't have to constantly try to beat the state of the art. In fact, that's kind of antithetical to science because all you're doing is chasing numbers.

A good real-life example of that is when students study very hard to memorize their notes so that they can ace their exam without truly understanding the material or how it's applied. When you're chasing only numbers, sometimes it's easy to forget why those numbers matter in the first place. Anyway, to get back to the point.

It's not always true that you want to compare to the state of the art. Sometimes if you just want to test whether or not something is working, for example as a proof of concept, then the simplest model possible should suffice. In Time series analysis, the simplest model possible happens to be the naive forecast. What is the naive forecast? Well, it's just another name for something we've already discussed, that is to copy the previous known value forward in time.

One interesting phenomenon that happens in Time series analysis is that a lot of bad models end up looking like naive forecasts. When you look at the model predictions from afar, they seem to be pretty close to the true values. But when you zoom in, you can see that they seem pretty close only because they're just copying the previous value or close to it.

A really bad situation is this: suppose that you fit a model and you say, “Aha, I beat the naive forecast because my accuracy is better than the naive forecast.” But of course, you have to ask, are you talking about the accuracy on the sample data or the out-of-sample data? Note that in machine learning we often refer to these as the training data and the test data. So I would use these terms interchangeably. Just be aware.

Well, one common mistake is that people believe because they got good accuracy on their in-sample data, that the same will be true for their out-of-sample data. And also, quite commonly, it turns out that the opposite is true. You might beat the naive forecast on the sample data, but on the out-of-sample data, the naive forecast beats you. Why does this happen? It happens when your model overfits to the noise in the training data, but doesn't actually generalize to the true underlying pattern in the Time series if one exists.

So that's why it's really important to compare your model to a baseline such as the naive forecast. It's not good enough to say, “I got 80 percent classification rate on my train and 75 percent on my test set.” If some other method achieves 70 percent on the test, then your model isn't as good.

There's one application I've seen a lot, which I think is a very interesting consequence of the times that we live in today. There are marketers everywhere on the Internet. The name of the game is SEO — search engine optimization. Everyone is trying to get clicks for their blog or to get people to sign up for their course or whatever. And of course, one of the obvious topics that many beginners care about is stock price prediction.

Now, if you're taking this course, then you know better. But let's continue the story. So imagine what happens. You take one of the most popular topics that would appeal to someone who doesn't know about finance, like stock predictions. You take one of the most popular machine learning algorithms that would appeal to someone who may not know a lot about machine learning, but has heard many buzzwords like LSTM. "LSTM" has been a very popular model for a sequence model. And then what do you do? Well, you combine these two, you make a blog post on stock predictions with LSTM. In fact, many people have done so. It's obviously a very appealing idea. No one would blame you for clicking on an article or buying a course that claims to be able to do this. I won't name any names, but there are some courses that make the very mistake I'm talking about in this lecture. Maybe you're watching this and you know where you've seen something like this yourself.

There is another even worse mistake that these marketers make. But we'll discuss that later when we talk about forecasting in general for a Time series. Models like Arima, if you want, you're encouraged to skip over to the forecasting lecture so we can continue this discussion.

To get back to the naive forecast, let's recall what we learned about random walks. As you recall, a random walk is where on every step of a Time series, I flip a coin or pick a number from a distribution. And that number is added to my current position in order to go to the next position. If my noise distribution is a zero-centered Gaussian with variance σ², which is not unreasonable, then the best forecast is the naive forecast. I can do no better than predicting the last known value.

Another way to think about this is if you build a model that you think is good but it cannot beat the naive forecast, then it might suggest that your model is actually worse than a random walk model. In other words, a random walk model describes the data better than your model.

**Notes:**

In this lecture, we discussed the importance of baselines in machine learning. A baseline provides a reference point for comparison. Without a baseline, a model's performance may seem impressive but could actually be worse than a simpler approach. For example, "if a linear model achieves 100 percent accuracy, then claiming 99 percent from a deep learning model isn't impressive."

In time series analysis, the simplest baseline is the naive forecast. The naive forecast works by copying the previous known value forward in time:

y_forecast[t] = y[t-1]

This approach is especially useful for random walk-like data, where the next value is essentially unpredictable and best estimated by the last known value.

A common pitfall is evaluating model performance only on in-sample (training) data. Sometimes a model may appear to beat the naive forecast on training data but fail on out-of-sample (test) data due to overfitting. This reinforces the importance of using naive forecasts as a baseline for generalization:

Example: Compare model predictions to naive forecast
naive_forecast = y_train[:-1]  # Previous values
model_error = np.mean((y_test - y_pred)**2)
naive_error = np.mean((y_test[1:] - naive_forecast)**2)

Another point discussed is the hype around stock price prediction using complex models like LSTM. Many beginner-level articles or courses claim great performance with sophisticated models but often fail to beat the naive forecast. This is because stock prices often resemble a random walk, meaning that predicting the last known value is often the optimal strategy:

Naive forecast for a random walk simulation
y_next = y_current  # Best estimate for the next time step

If a model cannot outperform the naive forecast, this indicates that the random walk model describes the data better than your complex model.

In essence, the naive forecast is a powerful and simple baseline. It reminds us that sometimes, simplicity is the most effective tool in time series forecasting, especially when data follows a random walk or exhibits strong stochastic behavior.

**Summary:**

The naive forecast is the simplest and often most effective baseline in time series analysis. It predicts the next value in a series as the previous value, making it particularly suitable for data that behaves like a random walk. Establishing a baseline is critical because it provides context to evaluate model performance and ensures that complex models truly offer improvement over simple heuristics. Many beginner-level approaches to stock prediction fail to outperform the naive forecast because financial time series are inherently stochastic. By comparing your model to the naive forecast, you can detect overfitting and evaluate whether your model captures true underlying patterns rather than noise. Ultimately, understanding and using naive forecasts instills the discipline of proper benchmarking and highlights that sometimes, simplicity is the most powerful strategy in forecasting.

**M) Naive Forecast and Forecasting Metrics in Code**

In this lecture, we are going to look at how to implement the naive forecast as well as evaluate it using the metrics we learned about.

OK, so let's start by importing "pandas".

The next step is to upgrade "scikit-learn". The reason for this is the current version of "scikit-learn" installed in Google Colab does not have the "mean_absolute_percentage_error" metric. So as I frequently mentioned in my courses, machine learning is a field that moves fast. This kind of thing is completely normal. Libraries change all the time.

The next step is to import our metrics from "sklearn" so we have the "mean_absolute_error", the "mean_squared_error", the "r2_score", and the "median_absolute_error". You'll notice that this does not include the "arm" nor the "SMAPE". We'll see how to deal with those later.

So for this exercise, we'll be using prices from the "S&P 500", which can be downloaded from my website. The next step is to call "pd.read_csv" in order to get a DataFrame of our data. As always, I'd like to do a "df.head()" to get some sense for the data we're working with. So we can see all the expected columns: "open", "high", "low" and so forth.

The next step is to generate our predictions. Basically, the naive forecast is a forecast where we simply predict the previous value. We can accomplish this by calling the "shift" function on the "close" column. And we'll call this new column "close_prediction". The next step is to call "df.head()" once again to see our new column. Notice that the first row now contains "NaN", since, of course, there is no last value for the first row.

OK, so for convenience, we're going to assign the true close prices to a variable called "y_true" and the predicted close prices to a variable called "y_pred". This is what these arguments are called inside "sklearn". So I felt it would be appropriate to call them the same thing.

OK, so the next portion of this notebook will be to look at our metrics. The main purpose of this is not just to understand how to do this in code, since that's pretty easy. But I want you to pay attention to how these values relate to each other. Think about what would be considered a good value and what would be considered bad.

OK, so let's start with the sum of squared errors. Since there's no function for this, we're going to calculate it ourselves. So since "y_true" and "y_pred" are effectively one-dimensional arrays, we can just take the difference and do a dot product with the same difference. OK, so the result is about 6000. Of course, we don't necessarily know whether this is bad or good. It's just a number.

The next step is to calculate the mean squared error using our "sklearn" function. OK, so this is the result. As you can see, this brings the number down to a more reasonable range. Now, as Python coders, we can't be afraid of implementing things ourselves. Some students get absolutely frightened when they see that you're not using a library. But I urge all students not to take this approach.

In fact, implementing the "MSE" is trivial. It's just what we had before, divided by the length of "y_true" or "y_pred". OK, and so we get the same answer as expected.

The next step is to calculate the root mean squared error. Now, surprisingly, this is done by the "mean_squared_error" function where you can pass in the argument "squared=False". So let's try that. OK, so we get about "1.67", which makes sense. And of course, we can just take the square root of our previous calculation, so let's try that also. And we get the same answer as expected.

The next step is to calculate the mean absolute error. Since we have a "sklearn" function for this, we are going to make use of it. OK, so you can see that although the root mean squared error and the mean absolute error have the same units, they do not give you the same value.

Now, we know that for all the previous metrics we've seen, they are scale-dependent. So the next step is to look at the "r2_score", which does not depend on the scale of the data. OK, so this should be surprising. As you recall, we said that the best "r2_score" is "1", whereas the "r2_score" of simply predicting the mean value is "0". It turns out that our naive forecast gets an "r2_score" of "0.999". This kind of makes sense since stock prices don't vary that wildly from one day to the next. So predicting the last value in the series should give us pretty good predictors. However, in another sense, these are also very bad predictions because they are really just the dumbest predictions possible.

So let this be a lesson that if you see a model that happens to predict stock prices very well, don't assume that such a model is actually useful.

The next step is to compute the "MAE", which is another scale-invariant and very symmetric metric. OK, so this is nearly zero, which makes sense since the "r2_score" is nearly one.

The next step is to compute the "SMAPE". Now you'll notice that I didn't import this function from "sklearn". This is because no such function exists. So this is the power of being able to implement these things yourself. Someone who does not have these skills would probably start by going to Google and then checking Stack Overflow and so forth. They might end up wasting their whole day trying to figure out where is the function for "SMAPE". But when you do have these skills, you're able to get this done in just a few lines of code and a few seconds of effort.

OK, and we see that the result is pretty close to the non-symmetric MAPE, which makes sense.

**Notes:**

In this lecture, we learned how to implement the naive forecast and evaluate it using common error metrics. First, we import the necessary libraries, i.e., "import pandas as pd".

Next, we ensure that scikit-learn is upgraded because the current version in some environments may not have the "mean_absolute_percentage_error" metric. This can be done with "!pip install -U scikit-learn".

Then, we import the metrics we need from scikit-learn using "from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score, median_absolute_error".

For this exercise, we use S&P 500 stock prices, which can be loaded as a DataFrame with "df = pd.read_csv('sp500.csv')" and we inspect the data with "df.head()". This shows columns such as "open", "high", "low", and "close".

The naive forecast predicts the previous value forward, which can be implemented using the shift function: "df['close_prediction'] = df['close'].shift(1)". Viewing the first few rows again with "df.head()" shows that the first row of "close_prediction" is "NaN" because there is no previous value.

For convenience, we assign the true and predicted values to variables using "y_true = df['close']" and "y_pred = df['close_prediction']".

Calculating Error Metrics

Sum of Squared Errors (SSE) – since there is no direct function, we calculate it manually with "sse = ((y_true - y_pred).dropna() ** 2).sum()".

Mean Squared Error (MSE) – can be calculated using scikit-learn with "mse = mean_squared_error(y_true[1:], y_pred[1:])".

Root Mean Squared Error (RMSE) – can be computed either by passing "squared=False" to the same function: "rmse = mean_squared_error(y_true[1:], y_pred[1:], squared=False)" or by taking the square root manually with "rmse = np.sqrt(mse)".

Mean Absolute Error (MAE) – a robust metric computed using "mae = mean_absolute_error(y_true[1:], y_pred[1:])".

R² Score – a scale-invariant metric that compares our model to simply predicting the mean, using "r2 = r2_score(y_true[1:], y_pred[1:])". Interestingly, the naive forecast can give a very high R² because stock prices change only slightly day-to-day.

Symmetric Mean Absolute Percentage Error (sMAPE) – there’s no built-in function, so we implement it manually with: "smape = np.mean(2 * np.abs(y_pred[1:] - y_true[1:]) / (np.abs(y_true[1:]) + np.abs(y_pred[1:]))) * 100". This ensures symmetry and handles percentage-based errors properly.

Overall, this exercise illustrates that the naive forecast is simple but surprisingly effective for financial time series, yet it also highlights that a high R² does not always imply a useful predictive model.

**Summary:**

The naive forecast is a simple baseline model where the previous value is used as the prediction for the next step, implemented easily using "shift" in pandas. It serves as an important reference to evaluate more complex models.

Error metrics such as SSE, MSE, RMSE, MAE, R², and sMAPE provide different perspectives: SSE and MSE are scale-dependent, RMSE is interpretable on the same scale as the data, MAE is robust to outliers, R² is scale-invariant, and sMAPE gives relative percentage errors.

In financial time series, naive forecasts often perform well in short-term predictions due to minimal daily changes, but this does not imply that they capture meaningful patterns. Comparing your model to the naive forecast ensures that it provides value beyond trivial predictions and helps prevent overfitting to noise.

**N) Time Series Basics Section Summary**

So in this lecture, we are going to summarize everything we learned in this section.

This section looked at time series basics which was designed to prepare you for the rest of the course.

We first started with a very simple question.

What is a time series?

Hopefully you now have a better understanding of what a time series is and what constraints must be met so that they apply to the methods we will study.

We next looked at the concept of modeling versus prediction.

This is an important distinction because sometimes we'll be focused on one and other times will be focused on the other.

You should now understand why modeling is useful and in fact can aid in prediction, especially when it gives you hints about when prediction is a waste of time.

The next step was to consider the shape of our data sets in this course, since we'll be working with Python and Python libraries.

There are certain conventions that we normally adhere to.

You should also now understand why having this reflex of automatically thinking about shapes will help your intuition in machine learning.

The next step was to discuss different time series tasks.

We looked at the one-step forecast, the multi-step forecast, and the multi-output multi-step forecast.

We also considered the practical applications of time series classification, which we will study in this course.

The next step was to learn about common data transformations used in Time series.

The transformations we studied all have a common property, which is that they tend to squash large values.

We learned about why this is a deeply fundamental operation reflected in nature itself.

We next learned about Time series metrics, which are more numerous compared to other fields of data analysis and machine learning.

This also taught us about one of the major themes of this course, which is that there are so many options to choose from.

Exercises for this course are essentially built in because there are many combinations.

We simply do not have time to try.

Your job in this course will be to try different combinations you think might work and see if you can obtain a superior result.

The next step for us was to turn our attention to Financial Time series.

We learned about important concepts such as the log price and the log return.

We then had a chance to do some practical work which involved simulating a stock price time series.

In the next lecture, we learned about why that practical work was useful when we studied the random walk hypothesis in depth.

We then learned about the naive forecasts and why it's extremely important to have baseline predictions for random walks in particular.

It turns out that the naive forecast is the best forecast.

The final exercise for this section was to implement the naive forecasts and to test out different metrics.

So hopefully you learned a lot and we'll see you in the next lecture.

**Notes:**

In this lecture, we summarize everything we learned in this section, which was designed to prepare you for the rest of the course.

We first asked the simple question: What is a time series? You should now understand that a time series is a sequence of observations indexed by time, and certain constraints must be met so that the methods we study in this course apply.

We then discussed the distinction between modeling versus prediction. Modeling is useful because it can provide insights into the underlying structure of the data and indicate when prediction might be futile. Prediction focuses on forecasting future values, often relying on modeling as a guide.

Next, we considered the shape of datasets in Python, since most time series methods in this course use Python libraries. Understanding shapes—i.e., the dimensions and arrangement of data—helps build intuition in machine learning and prevents errors when using functions like "numpy.reshape" or "pandas.DataFrame".

We explored different time series tasks:

One-step forecast: Predict the next value in the series.

Multi-step forecast: Predict several steps ahead sequentially.

Multi-output multi-step forecast: Predict multiple future values simultaneously.

We also discussed time series classification, which has practical applications such as predicting events or states based on sequences.

Next, we studied common data transformations, which generally have the property of squashing large values. These transformations help stabilize variance and are a fundamental concept seen in natural processes. Examples include "np.log()" for log transformations or "scikit-learn's StandardScaler" for scaling.

We learned about time series metrics, which are more numerous than in typical machine learning. Metrics include "mean_squared_error", "mean_absolute_error", "r2_score", "median_absolute_error", and "SMAPE". The abundance of metrics reflects a major theme of this course: there are many possible combinations, and your task is to experiment with these to find superior results.

We then shifted focus to financial time series, learning about log prices and log returns. We practiced simulating a stock price time series using Python: "lastP = np.log(P0); prices[t] = np.exp(lastP)". This exercise gave practical experience for the next topic.

We studied the random walk hypothesis, which models stock prices as unpredictable, Gaussian-distributed steps: "X[t] = X[t-1] + F[t]". We learned that in a random walk, the naive forecast—simply copying the previous value—is the best possible forecast.

Finally, we implemented the naive forecast and evaluated it with metrics such as "mean_squared_error", "mean_absolute_error", "r2_score", and "SMAPE". This exercise demonstrated the importance of baseline models in time series forecasting.

**Summary:**

This section provided a foundation in time series basics: understanding what a time series is, differentiating modeling from prediction, recognizing dataset shapes, and identifying different forecasting tasks.

You learned the importance of data transformations, multiple metrics, and how these apply to practical experiments.

In the financial time series context, you explored log prices, log returns, stock price simulation, and the random walk hypothesis. The section highlighted the significance of the naive forecast as a baseline, which is often the most effective forecast for a random walk.

By combining theory and practical Python exercises (e.g., "pd.read_csv", "np.log", "shift"), you now have a strong foundation to advance into more complex time series methods in the course.

**O) Suggestion Box**

So in this short lecture, I want to tell you about my suggestion box.

The idea behind this is analogous to the kind of suggestion box you would find at a restaurant.

You can write down your thoughts and leave them for the owner to look at to give them feedback so that they can improve your dining experience in order to share your thoughts with me and my suggestion box.

Please go to lazy programmers on slash suggestions.

Here you will find a simple form where you can tell me anything you like.

I have a few suggested fields, but none of them are required.

However, they would be helpful for me to know.

For example, tell me your background.

I think someone coming from a background in marketing is going to have very different feedback compared to someone coming from a Ph.D. in physics.

Tell me what course you are taking, so I have some idea of what you are talking about.

Obviously, the more specific you are, the better I can help you.

Tell me how difficult you thought the course was.

Was it too easy?

Was it too hard?

Tell me if there was something I neglected to explain.

For example, was there some word that I use that you have never heard of?

Was there Python code that you haven't seen before?

Tell me what you thought was missing from the course, even if it was just something small, like you missed explaining this line of code?

Were you looking for an algorithm that wasn't included?

This is helpful for me, but it's also helpful for you because many times students are looking for an algorithm or an explanation in the wrong course.

So I can say, actually, I teach that algorithm or I explain that thing in such and such course, and this isn't the right course.

So have a look over there.

Are there any topics you want to request that were not included in this course?

For example, maybe you signed up for a deep learning course and you were looking for CNN's, but the course didn't have CNN's in it.

Let me know.

Finally, let me know your suggestions for future courses.

If there's a particular topic you want me to teach that I don't yet have, of course, about, such as grading and boosting or transformers or even quantum mechanics.

Let me know.

Finally, there is a big text box for any comment you want to write.

You can write anything in this box and make it as long as you want.

In fact, the longer the better.

If you think I talked too slow, I talked too fast.

Let me know if you think my prerequisite instructions aren't fair.

Let me know.

I want you to be as specific and as detailed as possible.

A lot of the time people give me comments that I can't really act on, which is unfortunate.

And this is often because they are too generic and not specific enough.

Tell me exactly what lecture and exactly what time stamp you're referring to.

If you want to refer to a question on the Q&A, include a link.

Be very specific and give me concrete examples so that I know exactly how to act on the information you've given me.

Thanks for listening, and I'll see you in the next lecture.

**Notes:**

In this short lecture, the instructor introduces the concept of a suggestion box, analogous to the kind you might find at a restaurant. The purpose is to allow students to share feedback that can help improve the course.

Students are encouraged to visit Lazy Programmers → /suggestions to find a simple form where they can leave their thoughts. The form includes optional fields that are helpful for providing context:

Background: Your professional or academic background, e.g., marketing or Ph.D. in physics, since feedback may differ based on experience.

Course: Specify which course you are taking so the instructor knows what you are referring to.

Difficulty Level: Indicate whether the course was too easy, too hard, or just right.

Gaps in Explanation: Highlight terms, concepts, or Python code that were not fully explained.

Missing Content: Suggest algorithms, topics, or examples that were expected but not included in the course.

Future Course Suggestions: Recommend topics for upcoming courses, such as transformers, boosting, or quantum mechanics.

A large text box is available for detailed comments. Students are encouraged to be specific and detailed, including exact lecture numbers, timestamps, or Q&A links. This allows the instructor to act effectively on the feedback. General or vague comments are less actionable.

The instructor emphasizes that the more concrete and detailed the feedback, the more it can be used to improve the course. Students are encouraged to comment on pace, prerequisites, content clarity, missing algorithms, and other relevant course aspects.

**Summary:**

This lecture is about providing structured feedback via a suggestion box. Students can submit feedback about course difficulty, gaps in explanations, missing content, and suggestions for future courses.

The key points are:

Be specific about which lecture or timestamp you are referring to.

Include your background and course information for context.

Provide detailed examples to make feedback actionable.

Use the suggestion box to request topics not included or to propose new course ideas.

The goal is to create a two-way communication channel so the course can be continuously improved based on concrete student feedback.
