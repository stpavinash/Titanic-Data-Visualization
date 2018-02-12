# Titanic-Data-Visualization

Produced a visualization using tableau and the data-set included for the Titanic Data Visualization project.

NAME:  titanic3
TYPE:  Census
SIZE:  1309 Passengers, 14 Variables

DESCRIPTIVE ABSTRACT: The titanic3 data frame describes the survival
status of individual passengers on the Titanic.  The titanic3 data
frame does not contain information for the crew, but it does contain
actual and estimated ages for almost 80% of the passengers.

SOURCES: Hind, Philip.  "Encyclopedia Titanica."  Online.  Internet.
n.p.  02 Aug 1999.  Avaliable http://atschool.eduweb.co.uk/phind

VARIABLE DESCRIPTIONS:
pclass          Passenger Class
                (1 = 1st; 2 = 2nd; 3 = 3rd)
survival        Survival
                (0 = No; 1 = Yes)
name            Name
sex             Sex
age             Age
sibsp           Number of Siblings/Spouses Aboard
parch           Number of Parents/Children Aboard
ticket          Ticket Number
fare            Passenger Fare
cabin           Cabin
embarked        Port of Embarkation
                (C = Cherbourg; Q = Queenstown; S = Southampton)
boat            Lifeboat
body            Body Identification Number
home.dest       Home/Destination

SPECIAL NOTES:
Pclass is a proxy for socio-economic status (SES)
 1st ~ Upper; 2nd ~ Middle; 3rd ~ Lower

Age is in Years; Fractional if Age less than One (1)
 If the Age is Estimated, it is in the form xx.5

Fare is in Pre-1970 British Pounds (£)
 Conversion Factors:  1£ = 12s = 240d and 1s = 20d

With respect to the family relation variables (i.e. sibsp and parch)
some relations were ignored.  The following are the definitions used
for sibsp and parch.

Sibling:  Brother, Sister, Stepbrother, or Stepsister of Passenger Aboard Titanic
Spouse:   Husband or Wife of Passenger Aboard Titanic (Mistresses and Fiancées Ignored)
Parent:   Mother or Father of Passenger Aboard Titanic
Child:    Son, Daughter, Stepson, or Stepdaughter of Passenger Aboard Titanic

Other family relatives excluded from this study include cousins,
nephews/nieces, aunts/uncles, and in-laws.  Some children travelled
only with a nanny, therefore parch=0 for them.  As well, some
travelled with very close friends or neighbors in a village, however,
the definitions do not support such relations.

STORY BEHIND THE DATA: 
This dataset is based on the Titanic Passenger List edited by Michael
A. Findlay, originally published in Eaton & Haas (1994) Titanic:
Triumph and Tragedy, Patrick Stephens Ltd, and expanded with the help
of the internet community.  The original HTML files were obtained by
Philip Hind (1999).

PEDAGOGICAL NOTES:
This dataset is ideal for teaching basic functions in S-PLUS in the
realm of Statistical Computing and Graphics.  It can also prove useful
in teaching binary logistic regression and methods of imputation, both
single and multiple.  The dataset is also useful for demonstrating
many of the functions available in Frank Harrell's Hmisc library as
well as demonstrating binary logistic regression analysis using the
Design library.

An interesting result may be obtained using functions from the Hmisc
library in S-PLUS

attach(titanic3)
plsmo(age, survived, group=sex, datadensity=T)         # OR group=pclass
plot(naclus(titanic3))                                 # study patterns of missing values
summary(survived ~ age + sex + pclass, data=titanic3)

REFERENCES:
Harrell FE.  "Predicting Outcomes: Applied Survival Analysis and
Logistic Regression."  Book manuscript available from the University
of Virginia Bookstore, 1999.

SUBMITTED BY:
Thomas E. Cason, Undergraduate Research Assistant
Division of Biostatistics and Epidemiology
Department of Health Evaluation Sciences
University of Virginia School of Medicine
Box 600, Charlottesville, VA 22908 USA
Electronic Mail:  tcason@virginia.edu
