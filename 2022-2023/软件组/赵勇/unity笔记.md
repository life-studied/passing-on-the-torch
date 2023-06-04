Awake 当前控制脚本实例被装载的时候调用。一般用于初始化整个实例使用。 
Start 当前控制脚本第一次执行Update之前调用。 
Update 每帧都执行一次。这是最常用的事件函数。
FixedUpdate 每固定帧绘制时执行一次，和update不同的是FixedUpdate是渲染帧执行，如果你的渲染效率低下的时候FixedUpdate调用次数就会跟着下降。FixedUpdate比较适用于物理引擎的计算，因为是跟每帧渲染有关。
Update就比较适合做控制。 
LateUpdate 在每帧执行完毕调用，他是在所有update结束后才掉，比较适合用于命令脚本的执行。官网上例子是摄像机的跟随，都是在所有update操作完才跟进摄像机，不然就有可能出现摄像机已经推进了，但是视角里还未有角色的空帧出现。 
Reset 这个是编辑器模式情况下你点击reset按钮（如果有的话）调用的，你可以在这里做调试的初始化工作。
OnApplicationFocus OnApplicationPause OnApplicationQuit 应用程序失去焦点，应用程序暂停，应用程序退出时候发送这些消息。 
OnBecameInvisible OnBecameVisible 当脚本宿主（不）被任何摄像机显示时候发送此消息。 
OnCollisionEnter OnCollisionExit OnCollisionStay 当其他碰撞或者刚体（collider/rigidbody ）和参数的碰撞或者刚体（collider/rigidbody ）重叠、退出时发送前两个。而当他们保持重叠状态时每帧都会发送一个Stay消息。 
OnConnectedToServer OnDisconnectedFromServer OnFailedToConnect OnFailedToConnectToMasterServer 前两个 当客户端成功连接到服务器或者断开服务器时发送此消息。后两个当连接失败时候触发。 
  OnMasterServerEvent 当Master服务器发送报告时候触发。 
  OnNetworkInstantiate 当物体被Network.Instantiate时触发。 
  OnPlayerConnected OnPlayerDisconnected 在服务端当玩家成功连接/离线时候触发。 
  OnControllerColliderHit 当控制者和参数ControllerColliderHit碰撞时候触发此消息。官方举例可以用于角色移动一个物体，当角色碰到这个参数物体时候，你可以在这函数里操作移动此物体的动作。 
  OnParticleCollision 当粒子撞到碰撞体(collider)时触发。 
  OnDisable OnEnable 当脚本宿主被启用或者禁用时候触发。 
  OnDrawGizmos OnDrawGizmosSelected 编辑器状态时绘制Gizmos和Gizmos被选取时候触发。 (注：Gizmos参见我另一篇blog，他是用与做自己的组件时候用的，比如路径点绘制之类的。）
   OnGUI 绘制GUI时候触发。一般在这个函数里绘制GUI菜单。 
   OnJointBreak OnLevelWasLoaded 当新的level（Unity包）读取完毕时候触发。 
   OnMouseDown OnMouseDrag OnMouseEnter OnMouseExit OnMouseOver OnMouseUp 鼠标事件，都是当鼠标和gui或者碰撞体（Collider）交互时候触发。需要说明的是drag其实就是鼠标down后up之前持续每帧都会发送此消息。 
   OnPostRender 这个函数仅用于宿主为摄像机的脚本。当此摄像机范围内所有渲染都完成时候触发此消息。 
   OnPreCull 这个函数仅用于宿主为摄像机的脚本。当此摄像机剔除了某个渲染场景时候触发此消息。 OnPreRender 这个函数仅用于宿主为摄像机的脚本。当此摄像机开始渲染某个场景时候触发此消息。 
   OnRenderImage 当所有渲染完成image的postprocessing effects（只有pro版支持）后触发。 
   OnRenderObject 这个函数仅用于宿主为摄像机的脚本。当使用Graphics.DrawMeshNow 或者其他函数绘制自己建立的物体渲染完毕时触发。 OnSerializeNetworkView OnServerInitialized 当 Network.InitializeServer完成时触发。 
   OnTriggerEnter OnTriggerExit OnTriggerStay 当碰撞体(collier)接触触发区域（trigger）时候的一系列消息。 OnWillRenderObject
