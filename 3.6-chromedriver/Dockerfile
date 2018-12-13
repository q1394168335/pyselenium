FROM python:3.6

RUN apt update && apt install -y xvfb chromium unzip && rm -rf /var/lib/apt/lists/*

ADD xvfb-chromium /usr/bin/xvfb-chromium

RUN ln -s /usr/bin/xvfb-chromium /usr/bin/google-chrome && ln -s /usr/bin/xvfb-chromium /usr/bin/chromium-browser

RUN curl -SLO "https://chromedriver.storage.googleapis.com/2.45/chromedriver_linux64.zip" \
  && unzip "chromedriver_linux64.zip" -d /usr/local/bin \
  && rm "chromedriver_linux64.zip"

RUN pip install selenium -i https://pypi.doubanio.com/simple/

CMD python
