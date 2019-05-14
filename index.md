# NYC Motor Vehicle Collisions
<h1> TESTING </h1>
## Business Understanding (20 points)
- Identify, define, and motivate the business problem that you are addressing.
- How (precisely) will a data mining solution address the business problem?

## Data Understanding (5 points)
- Identify and describe the data (and data sources) that will support data mining to address the business
problem.

## Data Preparation (5 points)
- Specify how these data are integrated to produce the format required for data mining.

## Modeling (25 points)
- Specify the type of model(s) built and/or patterns mined.
- Discuss choices for data mining algorithm: what are alternatives, and what are the pros and cons?
- Discuss why and how this model should “solve” the business problem (i.e., improve along some dimension of interest to the firm).

## Evaluation (15 points)
- Discuss how the result of the data mining is/should be evaluated. How should a business case bedeveloped to project expected improvement?

## Deployment (10 points)
- Discuss how the result of the data mining will be deployed.
- Discuss any issues the firm should be aware of regarding deployment.
- Are there important ethical considerations? (this will depend on your project. There may be none)

## Presentation (20 points)
- Overall Communication/presentation and writing

You can use the [editor on GitHub](https://github.com/DavidKim01/DataAnalyticsProject/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/DavidKim01/MyGitPage/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

<!DOCTYPE html>
<html>

<head>

    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
        integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

    <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
        integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
        crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"
        integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1"
        crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"
        integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM"
        crossorigin="anonymous"></script>

    <title>Project Mishap</title>
</head>

<body>
    <div class="jumbotron jumbotron-fluid p-3 mb-2 bg-info text-white">
        <div class="container">
            <br>
            <h1 class="display-3">Project Mishap</h1>
            <br>
            <p class="lead">By Team Panda<br> Members: David Kim, Shashi Sasitharan, Mohammad Hassan, Wai Mun Liew,
                Xiaochuan Fang, Nittiya
                Nuanploy, Sujan Lamsal</p>
        </div>
    </div>

    <div class="container">
        <div class="row ">
            <h2 class="title"> Business Problem </h2>
        </div>
        <div class="row ">
            <div>The goal of this project is to minimize the injuries and deaths occurring due to vehicle collisions in
                New York City. The business problem here is to reduce the injuries and deaths due to vehicle collisions.
                We reduce this business problem into data mining problem by hypothesizing that the population of an area
                has a major say in determining the said injuries and deaths. We measure the impact population has on
                vehicle related deaths and injuries and extract a predictive value out of it.</div>
        </div>



        <div class="row">
            <h2 class="title"><br><br><br>Applications/business uses.</h2>
        </div>


        <div class="row">

            <div class="col"><br><br><br>Gives the city information on key areas/times collisions occur so they can
                implement more
                cameras or traffic enforcement in these areas that are more accident prone.
                If accidents occur at night for example in a specific area add more street lights there.
                Speeding : construct more stop signs or deploy speed traps where needed
            </div>
            <div class="col">
                <img src="Captured.PNG">
            </div>
        </div>

        <div class="row">
            <div class="col">
                <img src="Capture3.PNG">
            </div>
            <div class="col"><br><br><br><br>Our data could also be use to determines how much insurance companies
                should expect to
                charge for individuals on their premiums depending on various factors such as their vehicle type and
                what areas they will often drive
                in.
            </div>
        </div>

        <div class="row">
            <h2 class="title"><br>Linear Regression Model.</h2>
        </div>

        <div class="row"><br>
            We are using linear regression for year 2017 to predict 2018 and and making sure that our calculation is
            correct. After that we are going to use the same formula to predict 2019.
            <br>
            1. Run linear regression to see which variables has the most impact on collision.<br>
            2. Determine highly-influence factors from the variables that caused the collision.<br>
            3. Use other year historical data as training data to run cross validation to test our model
        </div>




        <div class="row">
            <h2 class="title"><br><br> Dependent Variables </h2>
        </div>
        <div class="row"><br>
            Out of all the fields, zip code is chosen as the population density of the zip codes are hypothesized to
            have the most predictive value. However, Population is not field in our database. So, we use another
            database that equates zip codes with their population. For this, we use Demographic Statistics by Zip Code
            database found in NYC Open Data website.
        </div>

        <div class="row">
            <div class="col"> <br>
                The target Variable is combination of<br>
                [NUMBER OF PERSONS INJURED]<br>
                [NUMBER OF PERSONS KILLED]<br>
            </div>
            <div class="col"> <br>
                <img src="Capture.PNG">>
            </div>
        </div>

        <div class="row">
            <h2 class="title"><br><br>Modelling With Linear Regression</h2>

        </div>
        <div class="row">
            The form of data mining used is supervised data mining. Our target field is labelled, and we know exactly
            what outcome we are trying to achieve. We use population of an area to predict the number of
            collision-related injuries and deaths in that area. Hence, we are utilizing predictive modelling.<br><br>
            In the project, we use linear regression model for predictive modelling. For this, we use a sum of the
            number of injuries and the number of deaths by zip codes as the dependent variable (y), and we use
            population of the zip codes as the independent variable (x).
	</div>
	<div class="row">
            <h2 class="title"><br><br>Modelling With Tree Classification Instead</h2>
        </div>
        <div class="row">
            We are using a classification tree to build our model. We will first divide the time into rush hour and midnight ranges to figure out which time frame has the most collisions. And then we are going to divide the date into holiday and non-holiday categories. Last we going to divide by the contributing factors. We going to calculate information gain (IG) and probability to determine which factor has the higher correlation.
	</div>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
	<div>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-indent: 36pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">We are using a classification tree to build our model. We will first divide the time into rush hour and midnight ranges to figure out which time frame has the </span><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: #ffff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">most </span><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">collisions. And then we are going to divide the date into holiday and non-holiday categories. Last we going to divide by the contributing factors. We going to calculate information gain (IG) and probability to determine which factor has the higher correlation.</span></p>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Classification Tree Calculations</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">PASSENGER VEHICLE, TIME, DATE, Holiday/not holiday, Driver Inattention/Distraction</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">First we need to find the entropy/information gain of each attribute </span></p>
		<ol style="margin-top: 0pt; margin-bottom: 0pt;">
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">(DONE)TOTAL(our target variable) parent </span></li>
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">(Done) WHO - PASSENGER VEHICLE, SPORT UTILITY / STATION WAGON, Other</span></li>
		<ol style="margin-top: 0pt; margin-bottom: 0pt;">
		<li style="list-style-type: lower-alpha; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;"> we need to get one side that is passenger and the other side is not passenger</span></li>
		</ol>
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">(Done)WHAT - (TIME)</span></li>
		<ol style="margin-top: 0pt; margin-bottom: 0pt;">
		<li style="list-style-type: lower-alpha; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">4 am to 4 pm</span></li>
		<li style="list-style-type: lower-alpha; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">4pm to 4 am</span></li>
		</ol>
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">WHEN - &nbsp;(DATE) Holiday/not holiday(need to extract and filter data) (yes or no)</span></li>
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">(Done) WHY - Driver Inattention/Distraction(need to extract and filter data) (yes or no)</span></li>
		<li style="list-style-type: decimal; font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">WHERE</span></li>
		</ol>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">No injury 86981/107248 = 0.81102677905</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Injury 20267/107248 = 0.18897322094</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ff0000; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">(parent) Total injured:</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-((86981/107248)*log2(86981/107248)+(20267/107248)*log2(20267/107248)) = 0.6993</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Morning total= 59689</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 49327/59689</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 10362/59689</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-((49327/59689)*log2(49327/59689)+(10362/59689)*log2(10362/59689))=0.6658737744598082</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Evening total = 47559</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 37654/47559</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 9905/47559</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-((37654/47559)*log2(37654/47559)+(9905/47559)*log2(9905/47559))=0.7381582939631328</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">INFORMATION GAIN (TIME)</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.6993 - ((59689/107248)*0.6658737744598082 + (47559/107248)*0.7381582939631328)</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #00ffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.0013717400201017783</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ff0000; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday/Not Holiday </span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday = 4282/107248</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 3445/4282</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 837/4282</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-((3445/4282)*log2(3445/4282)+(837/4282)*log2(837/4282))=0.7127738</span></p>
		<p><br /><br /></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Not Holiday = 102966/107248</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 83536/102966</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 19430/102966</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-((83536/102966)*log2(83536/102966)+(837/428219430/102966)*log2(837/4755919430/102966))=0.24476671</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">INFORMATION GAIN (Holiday/Not Holiday)</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.6993 - ((282/107248)*0.7127738 + (102966/107248)*0.24476671) = 0.4624317015379308</span></p>
		<p><br /><br /></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">passenger vehicle &amp; Non-passenger vehicle</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">passenger vehicle = 54405</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">non passenger vehicle = 52843</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(passenger vehicle) = 54405/107248=&gt;0.507282</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(non passenger vehicle) = 52843/107248=&gt;0.492717</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(passenger vehicle type did accident) =10183/ 54405 =&gt; 0.187170</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(passenger vehicle type did not accident)= 44222/54405 =&gt; 0.812829</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(NON passenger vehicle type did accident) = 10084/52843 =&gt;0.190829</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(NON passenger vehicle type did not accident)= 42759/52843=&gt;0.809171</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">entropy(passenger vehicle)=-[(10183/ 54405)(log(10183/ 54405))+(44222/54405)(log(44222/54405))]</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;-[( 0.187170)(-2.417579)+(0.812829)(-0.298976)]=&gt;-[-0.452498-0.243016]=&gt;0.695514</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">entropy(non passenger vehicle)=-[(10084/52843)(log(10084/52843))+(42759/52843)(log(42759/52843))]</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;-[(0.190829)(-2.389647)+(0.809171)(-0.305483)]=&gt;-[-</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.456014</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">-</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.247188</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">]=&gt;0.703202</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #f6b26b; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">information Gain(passenger vehicle type and non passenger vehicle type)</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 0.6993-[(0.507282)(0.695514)+(0.492717)(0.703202)]</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;0.6993-[</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.352821</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">+</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;"> 0.346480</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">]=&gt;0.6993-0.699301=&gt;</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #00ff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ff0000; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;"> passenger vehicle / STATION WAGON / other Vehicle Type</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Passage Vehicle total = 54405</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 10183 / 54405</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 44222 / 54405</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">: -((10183/54405)*log2(10183/54405)+(44222/54405)*log2(44222/54405))</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=0.6955142656715457</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">SPORT UTILITY / STATION WAGON total = 37738</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 30944 / 32632</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 6794 / 32632</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">: -((30944/32632)*log2(30944/32632)+(6794/32632)*log2(6794/32632)) </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt; text-indent: 36pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 0.5440203900702861</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Other Vehicle type = 15105</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 11815/ 15105</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 3290 / 15105</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">: -((11815/15105)*log2(11815/15105)+(3290/15105)*log2(3290/15105))</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 0.7561459696091096</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">INFORMATION GAIN</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.6993-((54405/107248)*0.6955142656715457+(37738/107248)*0.5440203900702861+(15105/107248)*0.7561459696091096)</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=0.0485533196397275366</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ff0000; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Driver Inattention and distribution / other contributing factor</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Driver Inattention/Distraction total = 32632</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 26432 / 32632</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 6200 / 32632</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">: -((26432/32632)*log2(26432/32632)+(6200/32632)*log2(6200/32632)) </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt; text-indent: 36pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 0.7014663313377333</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Other contributing factor = 74616</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Unharm = 60549/ 74616</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Harm = 14067 / 74616</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">: -((60549/74616)*log2(60549/74616)+(14067/74616)*log2(14067/74616))</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 0.6983761814407795</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffd966; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">INFORMATION GAIN</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.6993-((32632/107248)*0.7014663313377333+(74616/107248)*0.6983761814407795)</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=-0.0000164112952979656</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Total holiday = 4282</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday time -&gt; 4pm to 4 am </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 1966/4282</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy: 0.7578200750938036</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday time -&gt; 4am to 4 pm </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">= 2316/4282</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy : 0.6706551868879933</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Ig of holiday = 0.7127738</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.7127738 - ((1966/4282)*0.7578200750938036+(2316/4282)*0.6706551868879933)</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.7127738 - (</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.347938</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">+</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.362736</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">)=&gt; 0.7127738 - 0.710674=</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #00ff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">&gt;</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #00ff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.002099</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday ON Driver Inattention/other contributing factor</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Holiday = &nbsp;4282</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Driver Inattention_OR_Distraction on Holiday = 1296</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(Driver Inattention_OR_Distraction on Holiday / Holiday) = 1296/4282 =&gt; 0.302662</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">harmed_On Driver Inattention/Distraction = 242</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">unharmed_On Driver Inattention/Distraction = 1054</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p((harmed_On Driver Inattention/Distraction)/(Driver Inattention_OR_Distraction on Holiday))=242/1296</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p((harmed_On Driver Inattention/Distraction)/(Driver Inattention_OR_Distraction on Holiday))=1054/1296</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">other/Distraction on Holiday = 2986</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p((other/Distraction on Holiday) / Holiday)=2986/4282 =&gt;0.697338</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">harmed_On Driver Other contributing factor = 595</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">unharmed_On Driver other contributing factor =2391</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(harmed_On Driver Other contributing factor/(other/Distraction on Holiday)) = 595/2986 =&gt; 0.199263</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">p(unharmed_On Driver other contributing factor/(other/Distraction on Holiday)) = 2391/2986=&gt; 0.800737</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy(Driver Inattention/Distraction on Holiday)= -[(p(242/1296))(log(242/1296)) + (p(1054/1296))(log(1054/1296))]</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;-[(0.186728)(-2.420989)+(0.813272)(-0.298192)] =&gt;-[-0.452066 - 0.242511]</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;0.694577</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Entropy(other/Distraction on Holiday)=-[(0.199263)(log(0.199263))+(0.800737)(log(0.800737))]</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt;-[(0.199263)(-2.327254)+(0.800737)(-0.320599)]=&gt; -[-0.463736 -0.256715]=&gt;0.720451</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #00ff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">IG(Driver Inattention/other contributing factor ON Holiday)</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=0.7127738 - [(0.302662)(0.694577) + (0.697338)(0.720451) ] </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">=&gt; 0.7127738 - [(</span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffffff; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.210222)+ (0.502397)</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">] =&gt;0.7127738 - [0.712619]=&gt; </span><span style="font-size: 11pt; font-family: Arial; color: #333333; background-color: #ffff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">0.000155</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: #ffff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">.</span><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;"> &nbsp;</span></p>
		<p>&nbsp;</p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">From holiday to vehicle type</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Station dragon total=1535</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">unharm=298</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">harm=1237</span></p>

    	</div>
	<div>
		<h1 style="line-height: 1.2; margin-top: 24pt; margin-bottom: 0pt;"><strong><span style="font-size: 13.999999999999998pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Evaluation for Linear Regression</span></strong></h1>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Here, we get an R squared value of 0.572855, which shows that Population is a</span></p>
		<p style="line-height: 1.2; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">reliable indicator for predicting number of deaths and injuries due to vehicle</span></p>
		<p style="line-height: 1.2; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">collisions. </span></p>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-indent: 36pt; text-align: justify;">&nbsp;</p>
		<p style="line-height: 1.2; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">The equation we get from linear regression is:</span></p>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-indent: 36pt; text-align: justify;">&nbsp;</p>
		<p style="line-height: 1.2; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">18.543 + (x * 0.003834) where x is the feature you wish to predict</span></p>
		<h1 style="line-height: 1.2; margin-top: 24pt; margin-bottom: 0pt;"><strong><span style="font-size: 13.999999999999998pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">Deployment</span></strong></h1>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-indent: 36pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">The data we retrieved from our model can used by the New York City Department of Transportation to better understand their own roads. The DOT can use the data to deploy more traffic officers at the are more prone to accident. If the area have more store that need loading truck for transporting merchandise, the DOT could have the sign so that the track/van wont block the traffic. If it&rsquo;s due to drunk driving, traffic cops could set up checkpoint at places that have higher accident area. </span></p>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">The data is also very useful for automotive insurance corporations who can incorporate this data into their own model when determining the pricing for premiums based on vehicle and neighborhood in the NYC area. </span></p>
		<p style="line-height: 1.56; margin-top: 10pt; margin-bottom: 0pt; text-indent: 36pt; text-align: justify;"><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">We can use the data to predict when, where, and how </span><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: #ffff00; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">many collision</span><span style="font-size: 11pt; font-family: 'Proxima Nova',sans-serif; color: #353744; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;"> will happen in specific area in the NYC area, which can be used by the generic public. </span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">unharm=298</span></p>
		<p style="line-height: 1.38; margin-top: 0pt; margin-bottom: 0pt;"><span style="font-size: 11pt; font-family: Arial; color: #000000; background-color: transparent; font-weight: 400; font-variant: normal; text-decoration: none; vertical-align: baseline; white-space: pre-wrap;">harm=1237</span></p>
	</div>

</body>

</html>
