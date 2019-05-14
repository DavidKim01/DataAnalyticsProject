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
            <div> Our goal here is to use our data to predict when and where accident happen most ofthen.</div>
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
            <h2 class="title"><br><br>Linear Regression Model.</h2>
        </div>

        <div class="row"><br>
            We are using linear regression for year 2017 to predict 2018 and and making sure that our calculation is
            correct. After that we are going to use the same formula to predict 2019.
            <br>
            1. Run linear regression to see which variables has the most impact on collision.<br>
            2. Determine highly-influence factors from the variables that caused the collision.<br>
            3. Use other year historical data as training data to run cross validation to test our model
        </div>


        <div class="row"><br>


        </div>
        <div class="row">
            <div class="col"> <br>
                <h2 class="title"> Dependent Variables </h2>
            </div>

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

        <div>
        PASSENGER VEHICLE, TIME, DATE, Holiday/not holiday, Driver Inattention/Distraction

First we need to find the entropy/information gain of each attribute 
(DONE)TOTAL(our target variable) parent 
(Done) WHO - PASSENGER VEHICLE, SPORT UTILITY / STATION WAGON, Other
 we need to get one side that is passenger and the other side is not passenger
(Done)WHAT - (TIME)
4 am to 4 pm
4pm to 4 am
WHEN -  (DATE) Holiday/not holiday(need to extract and filter data) (yes or no)
(Done) WHY - Driver Inattention/Distraction(need to extract and filter data) (yes or no)
WHERE

No injury 86981/107248 = 0.81102677905
Injury 20267/107248 = 0.18897322094

(parent) Total injured:
-((86981/107248)*log2(86981/107248)+(20267/107248)*log2(20267/107248)) = 0.6993

Morning total= 59689
	Unharm = 49327/59689
	Harm = 10362/59689
-((49327/59689)*log2(49327/59689)+(10362/59689)*log2(10362/59689))=0.6658737744598082

Evening total = 47559
	Unharm = 37654/47559
	Harm = 9905/47559
-((37654/47559)*log2(37654/47559)+(9905/47559)*log2(9905/47559))=0.7381582939631328
INFORMATION GAIN (TIME)
0.6993 - ((59689/107248)*0.6658737744598082 + (47559/107248)*0.7381582939631328)
=0.0013717400201017783

Holiday/Not Holiday 

Holiday = 4282/107248
	Unharm = 3445/4282
	Harm = 837/4282
-((3445/4282)*log2(3445/4282)+(837/4282)*log2(837/4282))=0.7127738


Not Holiday = 102966/107248
	Unharm = 83536/102966
	Harm = 19430/102966
-((83536/102966)*log2(83536/102966)+(837/428219430/102966)*log2(837/4755919430/102966))=0.24476671

INFORMATION GAIN (Holiday/Not Holiday)
0.6993 - ((282/107248)*0.7127738 + (102966/107248)*0.24476671) = 0.4624317015379308



passenger vehicle & Non-passenger vehicle

passenger vehicle = 54405

non passenger vehicle = 52843

p(passenger vehicle) = 54405/107248=>0.507282

p(non passenger vehicle) = 52843/107248=>0.492717

p(passenger vehicle type did accident) =10183/ 54405 => 0.187170
p(passenger vehicle type did not accident)= 44222/54405 => 0.812829

p(NON passenger vehicle type did accident) = 10084/52843 =>0.190829

p(NON passenger vehicle type did not accident)= 42759/52843=>0.809171

entropy(passenger vehicle)=-[(10183/ 54405)(log(10183/ 54405))+(44222/54405)(log(44222/54405))]
=>-[( 0.187170)(-2.417579)+(0.812829)(-0.298976)]=>-[-0.452498-0.243016]=>0.695514

entropy(non passenger vehicle)=-[(10084/52843)(log(10084/52843))+(42759/52843)(log(42759/52843))]
=>-[(0.190829)(-2.389647)+(0.809171)(-0.305483)]=>-[-0.456014-0.247188]=>0.703202

information Gain(passenger vehicle type and non passenger vehicle type)= 0.6993-[(0.507282)(0.695514)+(0.492717)(0.703202)]
=>0.6993-[0.352821+ 0.346480]=>0.6993-0.699301=>0

 passenger vehicle / STATION WAGON / other Vehicle Type

Passage Vehicle total = 54405
	Unharm = 10183 / 54405
	Harm = 44222 / 54405

Entropy: -((10183/54405)*log2(10183/54405)+(44222/54405)*log2(44222/54405))
	=0.6955142656715457

SPORT UTILITY / STATION WAGON total = 37738
	Unharm = 30944 / 32632
	Harm = 6794 / 32632

Entropy: -((30944/32632)*log2(30944/32632)+(6794/32632)*log2(6794/32632)) 
= 0.5440203900702861

Other Vehicle type = 15105
	Unharm = 11815/ 15105
	Harm = 3290 / 15105

Entropy: -((11815/15105)*log2(11815/15105)+(3290/15105)*log2(3290/15105))
	= 0.7561459696091096

INFORMATION GAIN
0.6993-((54405/107248)*0.6955142656715457+(37738/107248)*0.5440203900702861+(15105/107248)*0.7561459696091096)
=0.0485533196397275366


Driver Inattention and distribution / other contributing factor

Driver Inattention/Distraction total = 32632
	Unharm = 26432 / 32632
	Harm = 6200 / 32632

Entropy: -((26432/32632)*log2(26432/32632)+(6200/32632)*log2(6200/32632)) 
= 0.7014663313377333

Other contributing factor = 74616
	Unharm = 60549/ 74616
	Harm = 14067 / 74616

Entropy: -((60549/74616)*log2(60549/74616)+(14067/74616)*log2(14067/74616))
	= 0.6983761814407795

INFORMATION GAIN
0.6993-((32632/107248)*0.7014663313377333+(74616/107248)*0.6983761814407795)
=-0.0000164112952979656

Total holiday = 4282

Holiday time -> 4pm to 4 am 
	= 1966/4282
	Entropy: 0.7578200750938036
Holiday time -> 4am to 4 pm 
	= 2316/4282
	Entropy : 0.6706551868879933

Ig of holiday = 0.7127738
0.7127738 - ((1966/4282)*0.7578200750938036+(2316/4282)*0.6706551868879933)

0.7127738 - (0.347938+0.362736)=> 0.7127738 - 0.710674=>0.002099

Holiday ON Driver Inattention/other contributing factor

Holiday =  4282

Driver Inattention_OR_Distraction on Holiday = 1296
p(Driver Inattention_OR_Distraction on Holiday / Holiday) = 1296/4282 => 0.302662
harmed_On Driver Inattention/Distraction = 242
unharmed_On Driver Inattention/Distraction = 1054
p((harmed_On Driver Inattention/Distraction)/(Driver Inattention_OR_Distraction on Holiday))=242/1296
p((harmed_On Driver Inattention/Distraction)/(Driver Inattention_OR_Distraction on Holiday))=1054/1296

other/Distraction on Holiday = 2986
p((other/Distraction on Holiday) / Holiday)=2986/4282 =>0.697338
harmed_On Driver Other contributing factor = 595
unharmed_On Driver other contributing factor =2391
p(harmed_On Driver Other contributing factor/(other/Distraction on Holiday)) = 595/2986 => 0.199263
p(unharmed_On Driver other contributing factor/(other/Distraction on Holiday)) = 2391/2986=> 0.800737

Entropy(Driver Inattention/Distraction on Holiday)= -[(p(242/1296))(log(242/1296)) + (p(1054/1296))(log(1054/1296))]

=>-[(0.186728)(-2.420989)+(0.813272)(-0.298192)] =>-[-0.452066 - 0.242511]
=>0.694577

Entropy(other/Distraction on Holiday)=-[(0.199263)(log(0.199263))+(0.800737)(log(0.800737))]
=>-[(0.199263)(-2.327254)+(0.800737)(-0.320599)]=> -[-0.463736 -0.256715]=>0.720451

IG(Driver Inattention/other contributing factor ON Holiday)=0.7127738 - [(0.302662)(0.694577) + (0.697338)(0.720451) ] 
=> 0.7127738 - [(0.210222)+ (0.502397)] =>0.7127738 - [0.712619]=> 0.000155.  

From holiday to vehicle type
Station dragon total=1535
	unharm=298
	harm=1237

        </div>




        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>



    </div>





</body>

</html>
