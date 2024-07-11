# Step

1. The "/admin/forms/option_lists/edit.php" page contains a "Import Option List" feature, which allows remote importing of a form.

2. The "/global/code/actions.php" file implements the functionality for making remote URL requests. Auditing the source code reveals that the request method can be manually specified, such as curl_exec().

   <img width="1031" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/aa258758-7743-48f2-ad7f-ef828cf251b9">

3. By sending a request and manually modifying the request method using Burp Suite, an SSRF vulnerability can be exploited. For example, the POC is “action=smart_fill&scrape_method=curl&url=file:///etc/passwd”.
   
<img width="955" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/0d45ac3f-3228-4c4e-93df-3df8664a6d7b">

<img width="1449" alt="image" src="https://github.com/DeepMountains/Mirage/assets/57616357/4af5e629-22d3-41b2-86d8-edb0bb31b027">


