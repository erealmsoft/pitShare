using angular-ui-bootstrap-datepicker

## show datetime
need to new Date(_dateTime), `_dateTime` is the value that from the server that store in DB

## take care of timezone
select the locale time, but send to the backend the utc time, without timezone information,
then the value returned from the backend is not the time that we want.
