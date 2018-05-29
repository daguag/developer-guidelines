# Maintenance Phase
[comment]:"reicht das hier erstmal?"

Which processes are needed after the publication of the app?

Your software components including backend services as well as the third-party components, modules, or services your software depends on is most likely to contain bugs or will get features added in the future.
Therefore an **update strategy** is required to distribute bug fixes and new features to your users. Simply offering a new version as a download on your website or in an app store might not suffice in case of critical updates [1]. Since security issues usually also effect the user's privacy, security issues should be handled responsibly [2].

The behavior of an app MUST correspond with the behavior stated in the PP/TOS. If new functions are added that exceed the areas defined in the original TOS and PP, then the PP/TOS MUST be updated and adjusted. Furthermore, the user MUST be informed about the change. In doing so, you SHOULD not only refer to general changes to the PP/TOS, but also to the changed area that will be made directly available to the user.
[comment]:"added from MTD"


**Monitor changes** to third-party components, modules, or services, as well as changes to the operating system. In addition monitor changes of terms of privacy policies of these components, as updating dependencies can impact the user's privacy. Furthermore legal requirements can change and new technologies or improvements to existing technologies for protecting the user's privacy might surface.

A plan for **disaster recovery** should also be in place. Security issues for your application or infrastructure might occur and should be handled appropriately. This includes a plan how customers are notified if their privacy was violated incidentally and to have a **backup strategy** to avoid loss of your customer's content.




---

**TODO**

- [ ] [1] Best practices for updating software
- [ ] [2] Best practices for handling security issues

