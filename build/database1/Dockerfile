FROM mysql:8
ADD build/mysql/nacos-mysql.sql /docker-entrypoint-initdb.d/nacos-mysql.sql
ADD build/mysql/tables_xxl_job.sql /docker-entrypoint-initdb.d/tables_xxl_job.sql
RUN chown -R mysql:mysql /docker-entrypoint-initdb.d/nacos-mysql.sql
RUN chown -R mysql:mysql /docker-entrypoint-initdb.d/tables_xxl_job.sql
EXPOSE 3306
CMD ["mysqld", "--character-set-server=utf8mb4", "--collation-server=utf8mb4_unicode_ci"]