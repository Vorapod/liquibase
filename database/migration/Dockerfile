FROM webdevops/liquibase:mysql

COPY ./ /liquibase

RUN cp -f /entrypoint /base-entrypoint.sh

COPY ./scripts/ /

RUN chmod +x /wait-for-it.sh
RUN chmod +x /entrypoint

ENV WAITING_FOR_HOST=company-a-db
ENV WAITING_FOR_PORT=3306
ENV WAITING_TIME=1

ENTRYPOINT ["/entrypoint"]