Troubleshooting
========

In rare cases, you might receive an error message when installing or updating WordLift. Here are some of the issues we gathered from our clients. 


Altervista blocking **WordLift** SaaS APIs
_____________

.. image:: /images/wordlift-troubleshooting-altervista-1.png

If WordLift is not working as expected, your key cannot be validated and you are using Altervista go to the *Server to Server* configuration in the Settings tab of your WordPress dashboard. 

.. image:: /images/wordlift-troubleshooting-altervista-2.png

Complete the identification procedure via SMS by adding your phone number. 

.. image:: /images/wordlift-troubleshooting-altervista-3.png

Now add `*.wordlift.it` in the whitelist (*.it*) and you are all set. WordLift can now interact with the backend APIs, your key gets validated and you are ready to WordLift your website.

========

While running the analysis I am receiving a Bad Request error
_____________

Typically this happens when the dataset of your website is corrupted (ie the post URI lacks the domain name).
`Contact the support <mailto:support@wordlift.io>`_ and we will rebuild your dataset. 