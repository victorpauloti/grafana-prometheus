# grafana-prometheus
     - ./prometheus.yml:/etc/prometheus/prometheus.yml
      - ./prometheus_data:/prometheus




      - '--config.file=/etc/prometheus/prometheus.yml'
      - '--storage.tsdb.path=/prometheus'
      - '--web.console.libraries=/etc/prometheus/console_libraries'
      - '--web.console.templates=/etc/prometheus/consoles'
      - '--web.enable-lifecycle'


      #ENTRYPOINT ["java -jar -Xms128M -Xmx128M -Dspring.profiles.active=prod target/forum.jar"]

      java -jar -Xms128M -Xmx128M -Dspring.profiles.active=prod target/forum.jar"