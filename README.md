# 🚀 ServiceMesh-Mapper - Microservices Communication & Dependency Visualizer

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg?logo=python&logoColor=white)  
![Tool](https://img.shields.io/badge/Dependency-Visualizer-FF5252.svg?logo=network)  
![Features](https://img.shields.io/badge/Features-Call%20Graph%20%26%20Latency-4CAF50.svg?logo=chart-line&logoColor=white)  
![Reports](https://img.shields.io/badge/Reports-JSON-2196F3.svg?logo=json)  
![CI/CD](https://img.shields.io/badge/CI/CD-Ready-2088FF.svg?logo=githubactions)  
![Dependencies](https://img.shields.io/badge/Dependencies-networkx%20%26%20matplotlib-green.svg?logo=python)

**ServiceMesh-Mapper** is a Python 3 tool designed to simulate inter-microservice calls, build a directed dependency graph, and visually map microservices communication flows with latency insights. It’s built for DevOps/SRE teams who want a quick visualization of service dependencies and communication patterns.

-------------

## 🛠 Tech & Languages

| Layer       | Tech / Format             | Purpose                                     |
|-------------|---------------------------|---------------------------------------------|
| Language    | **Python 3.10+**          | Core codebase                               |
| Core Logic  | `networkx` + `matplotlib` | Build and draw directed graph of service calls |
| Reports     | **JSON**                  | Data summary with nodes, edges, and latencies |
| Execution   | Script / Colab / Notebook | Flexible usage environment                  |
| Logging     | Console output + files    | Visual & data outputs for review             |

------

## 🌐 Architecture

Flow:  
1. Load `service_calls.json` containing simulated call events (caller, callee, latency)  
2. Build directed graph among services, accumulate call counts & latencies  
3. Generate `service_map_report.json` summarizing nodes & edges with metrics  
4. Draw the graph and save as `service_map.png` for visual inspection  
5. Use the report and graph for dashboards, CI/CD checks, architecture reviews  

---

## ▶️ Run ServiceMesh-Mapper

```bash
python service_mesh_mapper.py --events data/service_calls.json --output data/service_map_report.json
