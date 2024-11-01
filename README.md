# special-projects

## Table of Contents

- [special-projects](#special-projects)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [Purpose](#purpose)
  - [Projects](#projects)
    - [📂 AWS ECS Migration](#-aws-ecs-migration)
    - [📂 AWS EKS Migration](#-aws-eks-migration)
    - [📂 Design System Migration](#-design-system-migration)
    - [📂 Product Rebrand](#-product-rebrand)
    - [📂 Python to Node Services Migration](#-python-to-node-services-migration)

## Introduction

### Purpose

I have successfully led and coordinated various projects in my career. As a product leader, I have formulated successful go-to-market strategies and successfully delivered impactful features. The intent of this document is to highlight unique projects I owned that contributed to the organization’s success. While impactful, not all these projects were customer facing, but essential to meet corporate goals.

---

## Projects

| Project                              | Category         | Description                                                             |
| ------------------------------------ | ---------------- | ----------------------------------------------------------------------- |
| 📂 AWS ECS Migration                 | Devops           | Migration to AWS ECS.                                                   |
| 📂 AWS EKS Migration                 | Devops           | Migration to AWS EKS.                                                   |
| 📂 Design System Migration           | Design, Frontend | Migration of Design System from Fomantic to Flowbite with Tailwind CSS. |
| 📂 Product Rebrand                   | Design, Frontend | Product rebrand and ugrading the application appearance.                |
| 📂 Python to Node Services Migration | Backend          | Migration of backend services from Python to Node.                      |

### 📂 AWS ECS Migration

Migration consisted of migrating from physical servers to AWS Cloud Services. This migration was essential for meeting corporate goals and expanding business activities nationwide.

📄 **Background**:

The business served FIs (Financial Institutions) nationwide. The business primarily operated in the commercial lending space. Services included but were not limited to underwriting, document processing, appraisal management, data disaster recovery, etc. Operating in a highly regulated industry, security was top priority.

To provide secure file transfer and communication, the business developed an in-house solution to enable their services.

Corporate goals included a business expansion plan to increase revenue.

📄 **Problem**:

Physical servers were used for the data storage and deployment of the custom application. The servers were stored in secure lockers, hours from any corporate resource. This limited the business's ability to offer an attractive SLA. The company experienced longer than necessary outages due to this strategy. Server repair and maintenance required long drives that were not acceptable.

Corporate goals could not be met with this strategy.

In conclusion, a solution was needed for data storage, the mounting of RDBMS, and compute resources for application deployment.

🛠️ **Solution**:

Cloud services were identified as a feasible solution to the problems described. After reviewing different vendors, AWS (Amazon Web Services) was selected.

The AWS ecosystem offers numerous solutions, and the following were identified for this migration.

- **AWS ECS (Elastic Container Service)**\
  Amazon ECS is AWS's container orchestration to simplify the running, stopping, and managing of Docker containers.
- **AWS S3 (Simple Storage Service)**\
  Amazon S3 is an object storage service offering industry-leading scalability and data availability.

Migrating to cloud services would effectively optomize cost and decrease the risk of an outage. If an outage did occur, we had a better chance to recovery quicker than before.

🚀 **Outcome**:

The migration was successful.

This initiative was a large undertaking. Below are key items that had to be completed for a successful migration.

- Migrating production applications to the new infrastructure.
- Migrating production database.
- Migrating existing data and objects.
- Migrating analytics and reporting.

🚀 **Responsibilities and Lessons Learned**:

I was primarily responsible for managing cross-functional team dependencies and coordinating efforts. As the sole product leader of the organization, I played a pivotal role in the ongoing testing efforts in this migration. I possessed essential product knowledge that was vital for testing.

I was responsible for backlog prioritization and filtering existing bugs as testing occurred. This was vital for mitigating scope creep.

This was a major initiative that was very technical in nature. The organization had no experience with AWS and presented us all with a steep learning curve. This was an exceptional experience for me to learn about cloud technologies and more about the AWS ecosystem.

---

### 📂 AWS EKS Migration

This was a continuation of the [AWS ECS migration](#-aws-ecs-migration). Remaining in the AWS ecosystem, a shift was made from ECS (Elastic Container Service) to EKS (Elastic Kubernetes Service).

📄 **Background**:

The initial migration was a steep learning curve for the team. We successfully migrated to AWS but there was room for improvement. There was a change in leadership of the engineering team and development was moved in house. Our internal Devops resources had more experience with K8s (Kubernetes). ECS is known for simplicity and K8s offers some more robust features that includes auto-scaling and self-healing.

A decision was made to shift to K8s.

🚀 **Outcome**:

The outcome was successful.

All three environments were migrated to K8s. This also added some benefit to local development. The team constantly experienced local build issues and this effectively decreased the severity of this issue by 20%.

🚀 **Responsibilities and Lessons Learned**:

This was an exceptional experience for me. I got to work closely with Devops and learn more about infrastructure. As the sole product leader, I played a pivotal role in the ongoing testing as we were developing this infrastructure. This project took about six months. We had three environments where we had to migrate to EKS.

To effectively complete this migration, it required great context into the architecture of the entire application. Most of the application was built by external resources and the team lost context that was not documented when those resources left. I was one of the very left that had a good understanding of the entire application. As obstacles were encountered, I was a great resource to the devops engineer which was new to the team.

---

### 📂 Design System Migration

This migration consisted of efforts from the design team and the front-end development team. The migration consisted of migrating from Fomantic to Flowbite with Tailwind CSS.

📄 **Background**:

The product was developed on multiple design libraries that are listed below.

- **Semantic UI**: Learn more [here](https://semantic-ui.com/?ref=framestack).
- **Fomantic UI**: Learn more [here](https://fomantic-ui.com/).

The migration was due to the discontinued support for Semantic UI. Essentially, Fomantic UI began where Semantic UI ended. This was thought to be a seamless migration.

The business outsourced all design and most of the engineering talent. Talent was cycled often, context was easily lost, and documentation did not exist.

These libraries were chosen by business to save time in development, hoping to deliver value quicker.

📄 **Problem**:

The transition was not successful. Teams did not fully commit to this transition.

- **Developers used both Fomantic UI and Semantic UI**\
  Components were duplicated. While attempting to transition to Fomantic, teams continued to use the existing Semantic components. Conflict would occur when the design libraries collided. Conflict was resolved with patches rather than resolutions.
- **ONLY Fomantic styling was used**\
  The value was not realized from the open-source libraries. The business was under the assumption these components were easily dropped into the application code. While this was possible, development teams disagreed with the architecture of these components. Essentially, these components were JQuery components with a wrapper for compatibility with React. Development teams invested a lot of time in creating custom components that were inferior to the components they attempted to mimic.
- **Extended Development Periods**\
  Design teams were designing faster than engineering teams could develop. New problems were being solved with new components and nobody understood the need for longer development periods.
- **Development did not meet design specs.**\
  Following extended development periods, the output did not align with the original design.

🛠️ **Solution**:

The initiative was to align the design and engineering team. Buying a design system would save development time required to build custom components. A design system that offered pre-existing Figma files and React components was chosen to remove variation between design and development.

The design system was chosen as collective. This ensured it met the needs of design, engineering, and product.

🚀 **Outcome**:

The migration was a success.

- Teams were effectively aligned, establishing a level of communication that did not exist before.
- Product implemented a process to reduce the creation of custom components by both teams.
- Development output was increased.

🚀 **Responsibilities and Lessons Learned**:

I was primarily responsible for the coordination of the cross-functional teams and ensuring this project was successful. I managed the backlogs for both design and engineering to work through dependencies.

I did play a pivotal role in initiating this project. When I joined the team. I quickly noticed we had a problem and began interviewing team members. This created a list of symptoms disguised as problems. As time passed, I began doing some research in the code base. I developed some assumptions and asked my question differently to the new engineering manager. Together we quickly found the problem.

I began doing some market research and brought engineering and design leadership together. As a collective, we formulated a solution for our problem. I took this idea to senior leadership, explaining the cost-savings benefit. It quickly made sense, and they approved our idea for the migration.

While this area of concern is normally out of scope for a product leader, I was determined to understand our problem as an organization. This simple misunderstanding led to team misalignment and cost the business a lot of money.

In conclusion, the extended delivery times were thought to be an engineering problem, but it was organization problem. Succeed together and fail together. I effectively brought the teams together and we found success through collaboration.

---

### 📂 Product Rebrand

A product that instills UI/UX principles, promotes a beautiful cohesive product that is easy to use.

📄 **Background**:

I joined an organization that developed a solution for internal use only. Functionality was prioritized over visual appeal or experience. I was recruited to transform this product into a market fit.

📄 **Problem**:

The product was not a market fit. It had an incohesive experience that did not instill good UI/UX principles. Each page felt like a slightly different product.

🛠️ **Solution**:

To transform the existing product into a market-fit, we created a plan to promote a cohesive experience. Below are some of the steps taken.

- **Brand Guide**\
  A brand guide establishes guidelines for the proper user of brand logos, typography, and color palettes.
  A brand guide provides guidelines for a brand's identity and how it is to be presented. Elements found in a brand guide include imagery, logo usage, typography, and color palettes.
- **Style Guide**\
  A style guide provides guidelines for writing, design, and overall branding of the organization. Elements found in a style guide can consist of writing style, tone and voice, formatting, and standard nomenclature.
- **Global Pattern Guide**\
  By combining the brand and style guide, global patterns were established to promote a cohesive experience. These patterns created a standard way to solve UI/UX problems, improving the user experience.

A site map was created for the product which included approximately 70 pages.

🚀 **Outcome**:

The outcome was a success.

Through establishing the guides described above, we effectively rebranded the product, making it a market fit. The visual appeal was exceptional, and the user experience was enhanced significantly.

Prior to taking the product to market, we performed an internal survey. A survey was conducted both before and after the enhancements. The feedback from our internal users reflected a significant increase in satisfaction.

🚀 **Responsibilities and Lessons Learned**:

I was primarily responsible for creating a market-fit product.

The design team was responsible for rebranding and establishing a brand guide. I was responsible for establishing the style guide and global patterns through collaboration with our designer and technical writer.

This was an exceptional experience to rebrand a product. Most organizations have these patterns established and a product leader must operate within these guidelines. Our team had the privilege to own this initiative to create something new and beautiful. This was no easy task. We invested a lot of time in researching UI/UX principles and industry standards.

In conclusion, I had taken standards in mature organizations for granted. It was not until I experienced this that I learned to appreciate documented standards.

---

### 📂 Python to Node Services Migration

This was a backend project to migrate from the application API services from Python to Node.

📄 **Background**:

The backend services of the application were written in Python with synchronous programming. The team consisted mostly of Python developers until the business began exploring nearshoring and offshoring relationships. This shifted primary skillsets in the team from Python to Node and JavaScript.

Studies have shown that the same business logic can be developed with less code if written in Node instead of Python, effectively decreasing the time required for development. The asynchronous support in Node may make it a better fit for web development, offering higher performance for I/O (Input / Output Transactions).

📄 **Problem**:

There was a decline in available Python resources and an increase in Node resources on the team. There was a decline in delivery and investments were made in external resources. The external resources offered limited resources in Python programming.

🛠️ **Solution**:

To increase delivery, a decision was made to migrate the backend services from Python to Node. The expected outcome was to overcome resource limitations and create an architecture with high performance.

🚀 **Outcome**:

This was a very slow project. Very few resources knew both Python and Node well enough to migrate the services. Internal and external factors changed, moving all development in-house. The team was primarily skilled in Python and almost nobody knew Node.

This project was put on hold due to internal and external factors.

During this migration, new services were in Node. As development shifted in-house, this presented a problem for the team. Half of the services were written in Node and half of the Python services were rewritten in Node. The team made the decision that the current services would be supported but all new services would be written in Python.

🚀 **Responsibilities and Lessons Learned**:

This project was very technical and presented me with a steep learning curve. It was one of my first projects but laid the foundation for the development of my technical acumen.

The project required direction from the technical lead. The team doing the work had little insight into their next steps. Sprint planning or grooming was difficult, tickets had title with no information. This was not working. It was a new dynamic for me. I previously had written the tickets or the team could write their own technical tickets. I had to find a way to establish better collaboration between the technical lead and the team migrating the services. We as a group collectively found a path to promote accountability for each of us. The accoutability we agreed to helped us make future sprint plannings and groomings a success.
