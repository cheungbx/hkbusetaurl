# hkbusetaurl
 A web tool called “HK Bus ETA API url generator” that provides an input window that  take free form input of the following format:
e.g.
bus_company_id   route   direction   stop_name
KMB   234A   荃灣   海韻花園
KMB   234B   荃灣   海韻花園
KMB   234C   觀塘   海韻花園
KMB   234D   觀塘   海韻花園
KMB   261B   九龍站   海韻花園
KMB   48P   火炭   海韻花園
KMB   52P  旺角  海韻花園
KMB   53   荃灣   海韻花園
GMB   96C   荃灣   碧堤半島
KMB   52X   旺角   海韻花園
CTB   952   銅鑼灣 海韻花園
KMB   A38   機場   深井深慈街
GMB   308M   青衣站   海韻花園
KMB   52X   屯門   碧堤半島
KMB   53   元朗   碧堤半島
CTB   952   屯門   碧堤半島

Apply basic validation:
Bus_company_id  must be KMB CTB or GMB.
Then followed by 3 words separated by space (for values of route, direction, stop_name). Only Alphanumeric and Chinese Characters are allowed.
All lowercase input will be converted to upper case before further processing.

For each input line, based on the bus_company_id and route use  the  HK government bus eta API to find the stop ids with directions and  stop names beginning with the same characters as the direction and  stop_name provided by the input above.

Output the following input by user (bus_company_id   route   direction   stop_name). On the same line, append the url of the API that can be used by the user to retrieve the eta.
At the top of the output window, show a copy button to allow the output text to be copied to the clipboard.
Provide a window to allow each url for API to be tested.
