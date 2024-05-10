# moving betwen storage classes
You can transition objects between storage classes
for frequently accessed object move them to Standard IA
for archiving objects move them to galcier
moving objects can be automated by life cycle rules
Life cycle rules can  have transition actions , expiration actions
rules can be created for certain prefix
rules can be created for certain objects tag
![image](https://github.com/alsmk/SAA_notes/assets/43688097/3cbec628-1a5c-46e2-a6fd-0c582286db61)

![image](https://github.com/alsmk/SAA_notes/assets/43688097/76390497-d9f1-418f-b899-d436e3af3d1c)

# Baseline performance
your application can achieve at least 3500 put/copy/post/delete or 5500 get/head request per second per prefix in a bucket
tasks to do for optimize performance : multi part download(recommended for 100 mb, must apply for 5 gb), s3 transfer acceleration(happens through edge location)
