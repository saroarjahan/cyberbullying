# cyberbullying dataset
The first original dataset that we have used in this thesis was collected from Askfm
website1
. Askfm is mainly used for asking questions publicly and getting answers from
other Askfm users. Questions can also be asked anonymously. To collect each user’s
questions and answers, we have crawled each of the profiles using Python web crawler
library, Beautiful Soup2
. One possible way was to collect usernames by crawling
Askfm website’s home page. Askfm ’home’ page provides 20 random users for each
of the browser’s sessions. However, it is not guaranteed that all our collected users
would be English speakers. Therefore, we have only collected those usernames who
were located in UK, USA, and CANADA. For changing locations, we have used a
virtual private network (VPN). We have collected almost 3720 Askfm usernames to
put forward the next step, collecting questions and answers from each of the user’s
profiles.
Questions and answers associated with each user’s profile are saved in a CSV file.
Question-answer pairs of a profile are only extracted if they contain cyberbullying
swear words, further filtered by string matching technique. During the dataset
collection, we crawled 3720 user-profiles and over 400,000 question-answer pairs.
Applying swear words string matching technique reduced the data to 10k unique posts,
containing at least one swear words either in question or in answer.
We have manually labeled the resulting 10k Askfm dataset. Labeling involves
identifying whether each sentence contains cyberbullying or not. If the sentence
includes cyberbullying, we have given the label ’1’ and ’0’, if otherwise, examples
shown in Table 1. Once labeled, 21.3% of the dataset was identified as cyberbullying
and rest was not cyberbullying.
After labeling the dataset, we have identified 2k number of questions and answers
that contain cyberbullying. We have observed that user questions include 13% more
cyberbullying compare to the answers of those posts.
