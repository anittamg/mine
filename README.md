# How to test a Terraform Configuration?

**Among different methods terratest provides more comfortable tool for writing terraform unit tests. Terratest helps you automate this process like by deploying, validating, and un-deploying.**

**Steps:**

1. **Start by writing the test using Go in &quot; \*\_test.go &quot;, like for example instance\_test.go. We&#39;ll be attentive to make true or false assertions in our tests.**
2. **Then we&#39;ll write our Terraform code, describing our infrastructure, by trying to keep a modular structure of the project.**
3. **Use command &quot;** _ **go test \&lt;file\_name\&gt;.go&quot;** _ **eg:** _ **go test my\_test.go** _
4. **Terratest runs the tests. To validate the compliance of our infrastructure, the library might call HTTP endpoints, connect to machines via SSH, to execute commands, upload files, request Cloud Provider APIs and read Terraform outputs…**
5. **Finally, the tests infrastructure will be destroyed by terraform destroy.**
6. **Test results will be displayed in the console.**

**Environment Setup**

1. **Install terraform and connect with AWS with secret key and access key.**
2. **Install Go on your machine. Refrenence :** [**https://golang.org/**](https://golang.org/)
3. **Install / import the module that will be used to test Terraform
 dep ensure -add github.com/gruntwork-io/terratest/modules/terraform
 (not always work with all machines, if it doesn&#39;t work follow the next steps)
 Or like this with go get:
 go get github.com/gruntwork-io/terratest/modules/terraform **** (make sure git is installed in your machine else sometimes it through undefined error while trying to download dependencies
 reference for git installation :**[**https://git-scm.com/downloads**](https://git-scm.com/downloads)**)**
4. **Dependencies will be added in Gopkg.toml file, this also allows you to fix the version of the dependencies.**

**Structure of arranging files**

 **Recommended structure for arranging files**
 ![Tux, the Linux mascot](/assets/images/tux.png)
