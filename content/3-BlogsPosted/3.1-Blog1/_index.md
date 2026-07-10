---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# OPTIMIZING SECURITY WITH SESSION POLICIES IN AMAZON EKS POD IDENTITY

Amazon EKS Pod Identity provides a mechanism that allows Pods to securely access AWS services without managing static access keys. Recently, Amazon EKS added Session Policies, which allow inline IAM policies to be applied during the Pod's assumption of an IAM Role. This feature enables flexible permission scoping for each Pod while still leveraging existing IAM Roles, thereby simplifying permission management in large-scale Kubernetes clusters.

<div style="display:flex; justify-content:center;">
  <img src="/images/blogs/blog1.png" alt="Blog 1" style="width:80%; margin:8px 0;">
</div>

### Key points to know

- Session Policies are applied when the Pod assumes an IAM Role: The policy is used during the AssumeRole process to restrict the Pod's access to AWS resources without creating additional IAM Roles.
- Effective permissions are the intersection of the IAM Role and Session Policy: A Pod is only allowed to perform actions that are permitted by both the IAM Role and the Session Policy simultaneously. Session Policies cannot grant additional permissions — they can only narrow the existing permission scope.
- Simplifies IAM management: Multiple Pods can share the same IAM Role, while Session Policies are used to apply different permission levels for each workload, reducing the number of IAM Roles that need to be managed.
- Strengthens security through the Least Privilege principle: Each Pod's permissions are scoped exactly to its business requirements, minimizing risk when a Pod or application is compromised.
- Flexible deployment: Session Policies are configured through Pod Identity Associations and can be managed via the AWS Management Console, AWS CLI, or AWS SDK, enabling seamless integration into deployment and automation workflows.
- Suitable for large-scale Amazon EKS environments: Reducing the number of IAM Roles simplifies administration, prevents exceeding IAM limits, and improves scalability as the number of Pods or applications grows.

Session Policies are particularly useful in Microservices systems where multiple Pods share a single IAM Role but require different scopes of access to AWS resources. For example, one Pod may only need read access to a specific Amazon S3 Bucket, while another needs additional access to Amazon DynamoDB or Amazon SQS. By combining Pod Identity with Session Policies, the system maintains centralized management while ensuring each Pod has only the permissions necessary to perform its function.

[View post on AWS Study Group](https://www.facebook.com/share/p/1Bf61McbW7/)

---

### References

- [Amazon EKS Pod Identity – AWS Documentation](https://docs.aws.amazon.com/eks/latest/userguide/pod-identities.html)
- [Session Policies – AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#policies_session)
