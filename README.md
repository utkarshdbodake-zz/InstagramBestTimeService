# InstagramBestTimeService
For a given username/userid, analyzes the public instagram data and gives a good time to post (so that the user may get more likes.comments for his post).

To manually call the API:
Start the service locally.
Then Go to ipython & type below code:

import  requests, json
headers = {'content-type':'application/json'}
url = 'http://127.0.0.1:8000/find/best-time-to-post/'
data = {"id": "deepak365"}
params = {'content': json.dumps(data)}
response = requests.get(url, headers=headers, params=params)
if response.status_code == 200:
    print json.dumps(response.json(), indent=4, sort_keys=True)
else:
    print response
