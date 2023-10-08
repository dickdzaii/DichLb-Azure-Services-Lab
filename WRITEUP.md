# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

**Let's analyze some important benefits and limitations of both Virtual Machine and App Service to make the right decision for our CMS app**

*Virtual Machine*
>- Virtual machine is an IaaS (Infrastructure-as-a-service), which means we have to care about the infrastructure (like runtime or OS) and the app we develop.
>- Virtual machine is like a real computer with full access to the OS and installed software, it may provide more than what we need for a web app. 
>- The limitations of VMs are: they are more expensive than an App Service, and they are labor-intensive and time-consuming in management.

*App Service*
>- The App Service is a PaaS (Platform-as-a-service) which means we only care about our application and the data while Azure takes care of everything else.
>- It's an HTTP-based service for hosting web app, Rest API, and mobile backend, in our project, it's a web app. So App Service fits our needs.
>- Support multiple programming languages, including C# (ASP .NET and .NET Core) and Python, making it be the choice of most developers.
>- Support CI CD like Azure DevOps and GitHub, another point benefit because devs are familiar with them.
>- High availability and scalability, like VM.
>- Can control the cost with an App Service plan
>- The limitations are: 
>     - Limited Access to Host Server and unable to control the OS and software on server. This one does not affect much to our project since we just need to run it on browser and don't have to control the OS or any software,
>     -  Paying for the service plan, even if your services or application isn’t running: In my point of view, this CMS app runs 24/7, so it should be available all the time, as long as we have a reasonable plan, we can make our budget be controlled.
>     - Hardware Limitation: This limitation does not harm our project because it's just a lightweight app with non-high-performance computing needs.

Based on what we have analyzed, the App Service is the best choice for our application. It supports HTTP, web app, and mobile backend, high availability and scalability with Vertical and Horizontal scaling, and it is cheaper than VM. Using VM, still works for our app though, however, it's redundant and unnecessary because it provides some features that we don't need, and more important, it is more expensive than App Service.

### Assess app changes that would change your decision.

- With the benefits of VM, it would better for migrating from on-permises to the cloud, so if our software has already run with hardware server and we want to reduce the cost, then the VM should be the choice.
- If the application changes touch the limitations of the App Service, then we should consider changing the decision. If this application scales up to high performance requirements, or it has more features, then the App Service may not provide enough, that time the VM should be considered. Or if we want to control the Opearting System and the software on server or the application's programming language is not supported by the App Service, then we definitely need the VM.