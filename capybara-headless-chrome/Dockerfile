FROM ruby:2.4

# Install deps + add Chrome Stable + purge all the things
RUN apt-get update \
  # Install required packages
  && apt-get install -y apt-transport-https ca-certificates gnupg curl wget nodejs poppler-utils --no-install-recommends \
  # Install Google Chrome
  && curl -sSL https://dl.google.com/linux/linux_signing_key.pub | apt-key add - \
  && echo "deb [arch=amd64] https://dl.google.com/linux/chrome/deb/ stable main" > /etc/apt/sources.list.d/google-chrome.list \
  && apt-get update && apt-get install -y google-chrome-stable --no-install-recommends \
  # Remove extra files
  && rm -rf /var/lib/apt/lists/*
