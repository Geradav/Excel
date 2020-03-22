# Excel time intelligence functions

## Semester
_Retrieve the semester from a given date_

     =ROUNDUP(IMDIV(TEXT([Date],"M"),6),0)

_Retrieve the month number in the semester of a given date_

     =IF(MOD(TEXT([Date],"M"),6)=0,6,MOD(TEXT([Date],"M"),6))

_Retrieve the semester number from a start date and an end date_

     =ROUNDUP(IMDIV(DATEDIF(EDATE([StartDate],-1),[EndDate],"M"),6),0)
