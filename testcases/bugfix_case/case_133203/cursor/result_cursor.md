相关文件总结
主要 Bug 文件: pkg/scheduler/framework/preemption/preemption.go
涉及函数: PreemptPod, prepareCandidateAsync, prepareCandidate
队列管理: pkg/scheduler/backend/queue/scheduling_queue.go
事件处理: pkg/scheduler/eventhandlers.go
这个 bug 的核心是异步抢占中的错误处理逻辑不一致，导致 NotFound 错误被错误地传播，最终影响 preemptor pod 的正常调度流程。