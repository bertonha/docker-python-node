Docker base to use with you project with python and node projects eg. Django + AngularJS

Extending it:

    FROM bertonha/python_node

    RUN npm install -g bower coffee-script

    RUN pip install gunicorn

    ADD requirements/* /tmp/requirements/
    RUN pip install -r /tmp/requirements/production.txt

    WORKDIR /code
