# Step

1. 在"/admin/forms/option_lists/edit.php"页面中存在"导入选项列表»"功能，该功能允许远程导入一个表格。

2. "/global/code/actions.php"实现了去远程请求URL的功能，审计该源码发现可以手动指定请求实现的方法。比方说curl_exec()

   <img width="1031" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/aa258758-7743-48f2-ad7f-ef828cf251b9">

3. 发送请求，利用burpsuite手动修改请求方法， 可以实现SSRF漏洞。   POC “action=smart_fill&scrape_method=curl&url=file:///etc/passwd”

<img width="955" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/0d45ac3f-3228-4c4e-93df-3df8664a6d7b">

<img width="1449" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/4af5e629-22d3-41b2-86d8-edb0bb31b027">


