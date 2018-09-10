# via: https://qiita.com/hypermkt/items/c1cfe5f6e55a64c338d2

FROM ubuntu:12.04

# VOLUME ["/var/www"]

# PHP 5.3 + Apache で必要なパッケージをインストール
RUN apt-get -qq update \
    && apt-get install -y -qq --no-install-recommends \
      language-pack-ja-base \
      language-pack-ja \
      apache2 \
      libapache2-mod-php5 \
      php5 \
      php5-mysql

COPY default /etc/apache2/sites-available/default
COPY run /usr/local/bin/run
RUN chmod +x /usr/local/bin/run

EXPOSE 80
CMD ["/usr/local/bin/run"]
