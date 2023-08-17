<h1>Deploying a URL Shortener</h1>

<h2>How I went about deploying my application</h2>

<ol>
  <li>Downloaded the files from Kura and uploaded to a new repository which I named Deploy01</li>
  <img width="100" alt="dply1 1" src="https://github.com/NMonKLabs77/Deploy1.1/assets/139259756/db71f62d-b4c9-468d-bddd-8d79aa3ad5f7"><br>
  <li>Signed into the instructor's Jenkin's server</li>
  <li>Built the Jenkins pipeline </li>
 <img width="100" alt="jk" src="https://github.com/NMonKLabs77/Deploy1.1/assets/139259756/acc1261e-8878-416e-ab9d-20747cebfd3b"><br>
  <li>Created My EC2 and AWS ElasticBeanstalk</li>
    <img width="100" alt="aws" src="https://github.com/NMonKLabs77/Deploy1.1/assets/139259756/0fa16d25-df4e-40f1-b96a-380d704e0ae8"><br>
  <p>Upon submitting my elastic beanstalk environment, the health response was <em>Degraded</em></p>
  <h2>How I fixed the issue</h2>
  <ul>
    <li>I navigated to the elastic beanstalk logs to find out what the issue may be</li>
    <li>I requested that logs show me the last 100 logs</li>
    <li>I quickly went to ChatGPT to help me in finding the error from among the logs</li>
    <p>ChatGPT respnded with "No module named application"</p>
    
 <img width="100" alt="cgpt" src="https://github.com/NMonKLabs77/Deploy1.1/assets/139259756/daabec13-afae-48d2-be4b-0a2301dc2b3f"><br>
    <li>I went back to the zipped files I downloaded from my repository </li>
    <li>The main python application script was named "app.py" and not "application.py" so I renamed the file with the correct name.</li>
  </ul>
  <li>Terminated old EBS environment and configured a new one following all the previous steps but this time I used my zipfile with the modified "application.py" name change</li>
  <li>I ran my EBS environment and the Health responded with "OK"</li>
</ol>
<h2>My plan remains the same: </h2>
<img width="932" alt="dplychart" src="https://github.com/NMonKLabs77/Deploy1.1/assets/139259756/def2d4c8-2766-4e1d-b86e-e99c1d6187aa">





