# KurentoAndroidpeerVideoDemo
about WebRTC ,Kurento-Android-Client,Peer to Peer Video and in the room peers

# Bug
1. 订阅视频时，若响应错误，不能删除对应connection，导致不能再次请求订阅。建议onRoomError() 的参数携带 Request的Id，通过Id在本地保存的HashMap<id, user> 查找对应user，再根据user生成对应创建的connection进行删除，或直接建立HashMap<id,connection>的对应关系；
