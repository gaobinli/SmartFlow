### 项目描述
这是基于Spring Cloud Alibaba微服务架构的智能项目管理平台，通过项目创建、任务指派、自定义流程、角色权限管理等核心功能，实现企业项目全生命周期的流程化、智能化管控，提升项目管理效率。

### 技术栈
SpringCloud、Spring Boot、SpringCloud Alibaba、MyBatis-Plus、Redis、Nacos、Sentinel、RocketMQ、Gateway、Docker、WebSocket、JWT、SpringSecurity

### 工作内容
- **用户信息查询**：优化设计并实现基于TransmittableThreadLocal(TTL)的请求头拦截器，将Header数据封装到线程变量中，显著降低了约40%的用户信息数据库查询，同时集成了用户有效期自动刷新机制，优化用户会话管理体验。
- **Redis+Lua限流**：深度整合Redis与Lua脚本，实现了基于计数算法的精细化限流策略，能够有效抵御突发流量冲击。
- **服务降级与网关限流**：使用OpenFeign与Sentinel构建自定义Fallback服务降级方案，确保系统在服务异常时仍提供核心功能；同时利用Gateway结合Sentinel实施网关层面的流量控制，有效削峰填谷，防止单点服务过载，保障可用性。
- **Seata分布式事务落地**：为确保任务审批等流程中跨服务数据一致性，采用Seata分布式事务框架的AT模式，解决微服务架构下的数据一致性挑战。
- **接口鉴权体系搭建**：设计并开发基于自定义注解与AOP的服务接口鉴权与内部认证体系，实现细粒度的权限控制。
- **容器化环境部署**：采用Docker Compose搭建标准化项目环境，降低环境配置复杂度与差异性，实现容器化部署。
