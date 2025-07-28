需要修改的文件和函数
CRI API扩展文件: staging/src/k8s.io/cri-api/pkg/apis/runtime/v1/api.proto
涉及函数: RuntimeStatus消息定义
CRI API实现文件: staging/src/k8s.io/cri-api/pkg/apis/runtime/v1/api.pb.go
涉及函数: RuntimeStatus结构体相关方法
容器运行时接口文件: pkg/kubelet/container/runtime.go
涉及函数: RuntimeStatus结构体定义
运行时状态转换文件: pkg/kubelet/kuberuntime/helpers.go
涉及函数: toKubeRuntimeStatus
容器管理器文件: pkg/kubelet/cm/container_manager_linux.go
涉及函数: NewContainerManager
Cgroup管理器文件: pkg/kubelet/cm/cgroup_manager_linux.go
涉及函数: NewCgroupManager
kubelet主逻辑文件: pkg/kubelet/kubelet.go
涉及函数: updateRuntimeUp
运行时管理器文件: pkg/kubelet/kuberuntime/kuberuntime_manager.go
涉及函数: Status
配置类型文件: pkg/kubelet/apis/config/types.go
涉及函数: KubeletConfiguration结构体
指标定义文件: pkg/kubelet/metrics/metrics.go
涉及函数: 新增指标变量定义
Linux特定检查文件: pkg/kubelet/kubelet_linux.go
涉及函数: cgroupVersionCheck
配置示例文件: pkg/kubelet/apis/config/scheme/testdata/KubeletConfiguration/after/v1beta1.yaml
涉及函数: 配置参数更新