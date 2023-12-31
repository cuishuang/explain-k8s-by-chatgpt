# File: pkg/kubelet/userns/userns_manager.go

文件pkg/kubelet/userns/userns_manager.go是Kubernetes项目中kubelet组件中的一个文件，其作用是实现用户命名空间的管理。

userNsPodsManager是一个结构体，用于管理用户命名空间与Pod之间的映射关系。它维护了一个映射表，记录着每个Pod所使用的用户命名空间。

UsernsManager是一个结构体，用于管理用户命名空间的分配和释放。它维护了一个idMapping表，记录着用户命名空间的使用情况。

userNamespace是一个结构体，表示用户命名空间的相关信息，包括名称、uid、gid等。

idMapping是一个结构体，表示用户ID映射关系，包括源用户ID和目标用户ID。

writeMappingsToFile是一个函数，用于将用户ID映射关系写入到文件中。

readMappingsFromFile是一个函数，用于从文件中读取用户ID映射关系。

MakeUserNsManager是一个函数，用于创建UsernsManager对象。

recordPodMappings是一个函数，用于记录Pod与用户命名空间的映射关系，并将其加入到userNsPodsManager中。

isSet是一个函数，用于检查用户ID是否已被设置。

allocateOne是一个函数，用于分配一个未使用的用户命名空间。

record是一个函数，用于记录用户命名空间的使用情况。

Release是一个函数，用于释放一个用户命名空间。

releaseWithLock是一个函数，使用锁来释放一个用户命名空间。

parseUserNsFileAndRecord是一个函数，用于解析用户ID映射文件并将其记录到idMapping表中。

createUserNs是一个函数，用于创建用户命名空间。

GetOrCreateUserNamespaceMappings是一个函数，用于获取或创建用户命名空间的映射关系。

CleanupOrphanedPodUsernsAllocations是一个函数，用于清理孤立的Pod用户命名空间分配。

