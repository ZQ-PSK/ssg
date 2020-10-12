---
title: "User authentication journey"
weight: 5
description: "User authentication journey"
url: blog-sample
---
# User authentication and authorization

Users who interact with your services need a way to secure their actions and ensure that no third party accesses their personal data without consent.  
This can be achieved in a number of ways, and different levels of security can be applied to different kinds of operations.

Authentication and authorization are sometimes treated as synonyms. However, they are two very different concepts.

### Authentication
Answers the question *who is that user?*  
In user-oriented contexts, authenticating is usually called *logging in* or *signing in*. 
### Authorization
Answers the question *what is the user allowed to do?*  
Users may belong to different access groups or have different roles assigned. Each role or group has different *permissions* that manage what operations the user is allowed to perform.

A user must authenticate before they are authorized to act. Some levels of authorization require additional authentication.

## Risk-based authentication

With the emergence of powerful cloud computing, it became possible to analyze user behavior in minute detail. This enables authentication based not only on logins and passwords, but also behavior patterns.

Risk-based authentication makes use of algorithms that recognize non-typical actions from the user, such as logging in from another device, another country, or even interacting with the UI in an unusual way.

If an anomaly is detected, the policy may require that an action is blocked or confirmed through another channel. For example:
- When a user tries to make a bank transfer from a country where they have never logged in before, the bank calls that user and asks for additional authentication details.
- When a user logs in to their inbox from a new device, they receive a text message with a confirmation code or generate the code in an authenticator app.

The defense mechanism can also be adjusted for different roles - a regular user logging in from a new device is asked to provide a code, but a system administrator will have their account locked until another administrator confirms the identity.

## User authentication progress

In a traditional approach, a user provides a large amount of data upon registration: name, surname, date of birth, and so on. That data is very often collected even when there is no use for it.  
Such a way of processing user data is at a higher risk of:
- breaching data protection laws by excessive collection,
- leaking a set of data that provides all information needed, for example, for spear-phishing attacks,
- discouraging the user from proceeding.

To mitigate this, users should only be asked to provide the data that is needed, when it's needed, and be allowed to decide how long the data can be stored.  

Consider an example of a newspaper portal that publishes two kinds of articles: free to access (with a monthly limit) and those limited to paying users. The following progressive authentication policy could be applied:
- A user who wants to read free articles only needs to agree to a cookie that stores their UUID (used to keep track of how many articles the user read in the last 30 days).
- A user who wants to comment on articles must do the above, create a login, and create a password-protected account.
- A user who wants to buy a subscription must do both of the above, provide their personal details (such as their email and credit card data), and secure the account with multi-factor authentication (MFA).

In this scenario, the users are only asked to provide identification details that are necessary for the scope of actions they want to perform. This improves the security of their personal details, creates less sensitive data for you to store, and improves user experience.

The following chart shows the same example, with MFA requested for new devices after a user provides their personal data:

<figure><img src="/images/access-flow.png"/><figcaption style="text-align:center;font-size:0.8em;font-style:italic">Example access levels progress</figcaption></figure>

## Challenges in authentication

### User experience

Your users expect seamless and effortless work with the product.  Authentication may stand in the way of this, creating a conflict between user experience and user security.  
This could cause users to disable or ignore some security policies and make data vulnerable to attacks.

Some challenges that users may encounter include:
- frequent password change requirements,
- MFA reliant on a device that can be damaged, lost, or stolen,
- frequent login prompts,
- latency

### Technology

Passwords and codes are not the only ways of authenticating users.

A person can also be identified by scanning their face, fingerprints, or recognizing their voice. These techniques are becoming standard in consumer devices, but are not perfect and can be circumvented.

For example, a fingerprint scanner can be "tricked" with a silicone mold, or a photograph can be used instead of an actual face.