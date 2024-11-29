# prometheus-grafana-docker-compose
Locally, Grafana and Prometheus are started via Docker Compose to monitor the programs launched on my local machine.

使用步骤：

1. 创建一个新目录，例如 `monitoring`
2. 在目录中创建 `docker-compose.yml` 文件，粘贴第一个工件的内容
3. 创建 `prometheus` 子目录
4. 在 `prometheus` 目录中创建 `prometheus.yml` 文件，粘贴第二个工件的内容
5. 在该目录下运行：
   ```bash
   docker-compose up -d
   ```

访问地址：
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000 (默认用户名/密码: admin/admin123)

注意事项：
- 如果您的应用需要被监控，需要在应用中集成 Prometheus 客户端库
- 在 Prometheus 配置文件中添加您应用的 metrics 抓取配置
- 在 Grafana 中添加 Prometheus 作为数据源

