# Excel time intelligence functions

## Semester
_Retrieve the semester from a given date_

     =ROUNDUP(IMDIV(TEXT([Date],"M"),6),0)

_Retrieve the month number in the semester of a given date_

     =IF(MOD(TEXT([Date],"M"),6)=0,6,MOD(TEXT([Date],"M"),6))

_Retrieve the semester number from a start date and an end date_

     =ROUNDUP(IMDIV(DATEDIF(EDATE([StartDate],-1),[EndDate],"M"),6),0)

## One-off calculation
_Returns 1 only for the first date and zero for all other dates_
\nUseful when forecasting expenses based on an expense periode variable

     =N(MOD(DATEDIF([StartDate],[EndDate],"M"),9999)=0)
