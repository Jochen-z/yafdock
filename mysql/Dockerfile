ARG MYSQL_VERSION=8.0
FROM mysql:${MYSQL_VERSION}

MAINTAINER jochendev <jochenzhang94@gmail.com>

#####################################
# Set Timezone
#####################################

ARG TZ=UTC
ENV TZ ${TZ}
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

#####################################
# MySQL startup configuration
#####################################

ADD my.cnf /etc/mysql/conf.d/my.cnf

RUN chown -R mysql:root /var/lib/mysql/


CMD ["mysqld"]

EXPOSE 3306
