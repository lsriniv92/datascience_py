## NASA - HTTP

### Description:
The log traces contain two month's worth of all HTTP requests to the NASA Kennedy Space Center WWW server in Florida.

### Format:
The logs are an **ASCII file with one line per request**, with the following columns:
1. **host** making the request. A hostname when possible, otherwise the Internet address if the name could not be looked up.
2. **timestamp** in the format "DAY MON DD HH:MM:SS YYYY", where DAY is the day of the week, MON is the name of the month, DD is the day of the month, HH:MM:SS is the time of day using a 24-hour clock, and YYYY is the year. The timezone is -0400.
3. **request** given in quotes.
4. **HTTP reply code**.
5. **bytes in the reply**.

### Type of Data:
Unstructured data

### Dataset:
<ftp://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html>

### Goal:
To convert the unstructured data to structured data (dataframe)

### Input:
'in24.inetnebr.com - - [01/Aug/1995:00:00:01 -0400] "GET /shuttle/missions/sts-68/news/sts-68-mcc-05.txt HTTP/1.0" 200 1839\n'

### Output:

| hostname         | timestamp                  | http_request    |http_reply_code  |bytes_in_reply  |
| -------------    |:-------------:             | -----:                                              |---:|----:|
| in24.inetnebr.com| 01/Aug/1995:00:00:01 -0400 | GET /shuttle/missions/sts-68/news/sts-68-mcc-05.txt |200 |1839 |
