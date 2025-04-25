# Global field standards

## Overview

Our WOW has a primary focus of empowering teams to deliver more value for our customers through the establishment of standards, like global field standards, and tooling that promote seamless collaboration thereby increasing productivity and efficiency. Utilizing global field standards:

1. Helps streamline and enhance automation.
2. Empowers teams to collaborate effortlessly with actionable data insights.
3. Utilizes the tooling that promotes flexibility, consistency and ease of use across teams.

> [!TIP]
> Check out the [Our WOW data adoption tiers](../our-wow-data-adoption-tiers/our-wow-data-adoption-tiers.md) for different work item types and use this page for guidance on field values.

## Glossary

- **ADO**: Azure DevOps. The Azure DevOps team provides their own thorough [documentation](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/organization-management?view=azure-devops) for additional details.
- **Organization**: The specific ADO instance which you use. MSAzure, MSAzureDev, and Microsoft are all examples of commonly used organizations.
- **Project**: Projects are logical groups of work that help separate groups on an organization. One, OS, Universal Store, are all projects.
- **Semester**: A cross-company effort to envision and agree on the upcoming engineering efforts within Azure every six months.
- **Developer (Dev) Days**: The number of days it takes a developer to complete the work it describes.

## Azure ADO Global work item field specifications

Our goal is to align to a set of global fields for work items across multiple Azure ADO organizations. The purpose of these fields is to make work management predictable and enable better decision making in prioritization and execution.

| **Field name** | **Description** | **Type** | **Values** | **Applicable work item types** |
| --- | --- | --- | --- | --- |
| Title | One line description of the work. It should be a logical name/phrase for the work. More details [here](../../TeamPlanningBasicsPlaybook/team-planning-basics-playbook/team-planning-basics-playbook.md#title-guidance). | Text |  | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li><li>Task</li><li>Bug</li> |
| Description | One to three sentences of information that provides background on the work and what it's intended to accomplish. | Text |  | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li><li>Task</li> |
| State | Current status of the work item. As this work item changes, it should be updated appropriately in the day that it changes. | Dropdown | <li>"New" - Created but not yet committed nor started.</li><li>"Committed" - Agreed to work on (to be completed within the iteration) but not yet started.</li><li>"Active" - Work on this has started or is underway.</li><li>"Closed" - Work is complete.</li><li>"Removed" - No longer committed nor worked on.</li> **Note: The above values are the standard state field that teams should aspire to use. There may be other custom values included in your specific project that are not included above. Find more details about state standards [here](../state-standards/state-standards.md).** | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li><li>Task</li><li>Bug</li> |
| Assigned to | Who is working on the item. | Identity | Person name selection | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Area path | The ADO work location for the team. Setting the Area path correctly is what puts the item on the team's backlog. | Dropdown | Select an area path. Area paths are defined by the [area path guidance](../../AreaPathGuidance/area-path-guidance/area-path-guidance.md) and managed/created with the [Areas extension](../../../ExtensionsAndTools/OwnershipService/areas/areas.md). | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li><li>Task</li><li>Bug</li> |
| Iteration path | The iteration when the Feature is targeted to complete. | Dropdown tree | Select from Azure's [standard iteration paths](../../iteration-standards/iteration-standards.md). | <li>Objective</li><li>Key Result (KR)</li><li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li><li>Task</li><li>Bug</li> |
| Classification | List of broad cross org initiatives to which this work is accrued. | Dropdown | Check out [the Classification and Sub Classification values](../../WorkItemTypesAndFieldsStandards/classification-and-sub-classification/classification-and-sub-classification.md). | <li>Bug</li><li>Epic</li><li>Feature</li> |
| Commitment Reason | If Commitment Status is "Deferred" or "Rejected", add comments. | Dropdown | <li>Dependency on another team</li><li>"Head count constraint"</li><li>"Not a Priority"</li><li>"Not a valid ask"</li><li>"Submitted after deadline"</li><li>"Duplicate"</li> | <li>Epic</li><li>Feature</li> |
| Commitment Status | Field to indicate commitment of work item. This should be used instead of Partner Ask Status field and is applicable to all work, not just dependencies. | Dropdown | Learn more about Commitment Status field values [here](#how-do-i-effectively-use-commitment-status-field-values). | <li>Epic</li><li>Feature</li> |
| Completed work | Completed work in **Dev days**. | Integer |  | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| GA Date | Date in which feature will be available for General Availability | Date |  | <li>Epic</li><li>Feature</li> |
| Original Estimate | Original Estimate at the time of planning the work. Unit - **Dev days**. | Integer |  | <li>Epic</li><li>Feature</li> |
| Priority | Priority of this work item relative to other items in the backlog. | Dropdown | <P><li>"0" - Must complete this work item within iteration/semester. Other work is dependent on this.</li><li>"1" - Should complete this deliverable within the iteration/semester</li><li>"2" - Nice to have. Not critical for this iteration/semester. There is dependent work on this deliverable.</li><li>"3" - Nice to have. Not critical and no dependency. There is no work dependent on this delivery</P> | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Private Preview Date | Date in which feature will be available for Private Preview | Date |  | <li>Epic</li><li>Feature</li> |
| Public Preview Date | Date in which feature will be available for Public Preview | Date |  | <li>Epic</li><li>Feature</li> |
| Remaining Work | Remaining work in **Dev days**. | Integer |  | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Risk Assessment | Indicates whether a work item is "On Track" or not. | Dropdown | <li>"At Risk" - Confidence for completing the work is low.</li><li>"Off Track" - Corrective action is required to get the work on track.</li><li>"On Track" - Work is going as planned and high confidence for delivery.</li> | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Risk Assessment Comment | Add comments for work items that have Risk Assessment of "Off Track" or "At Risk". | HTML |  | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Severity |A consistent way to view and act upon severities across initiatives.|Dropdown|Severities map to <https://aka.ms/azurecen> where applicable.|<li>Bug</li>
| Service ID | Service Tree ID of the service responsible for the work. | Text |  | <li>Epic</li><li>Feature</li> |
| Service Name | Name of the service responsible for the work as it appears in Service Tree. | Text |  | <li>Epic</li><li>Feature</li><li>Product Backlog Item (PBI)/User Story</li> |
| Status | The Status field enables teams to accurately track a deliverable (Epic/Feature) through a consistent set of delivery milestones/steps. | Dropdown |  | <li>Epic</li><li>Feature</li> |
| Sub Classification | List of initiatives within its parent initiative. | Dropdown | Check out [the Classification and Sub Classification values](../../WorkItemTypesAndFieldsStandards/classification-and-sub-classification/classification-and-sub-classification.md). | <li>Bug</li><li>Epic</li><li>Feature</li> |
| Target Date | Date when the consuming team is requesting completion. | Date | Date | <li>Feature</li> |

## What standard fields are used when creating and managing dependencies?

Below is the "schema" work items utilize for [dependency creation](../../../ExtensionsAndTools/DependencyTracker/create-dependency/create-dependency.md) and [dependency triage](../../../ExtensionsAndTools/DependencyTracker/dependency-dashboard/dependency-dashboard.md#triage-dependencies).

If requestors are using [Dependency Tracker](../../../ExtensionsAndTools/DependencyTracker/dependency-tracker/dependency-tracker.md) to create dependencies, the tool sets defaults for some of these fields. If requestors are [linking work items manually](../../../ExtensionsAndTools/DependencyTracker/create-dependency/create-dependency.md#manual-dependency-creation-microsoftos-only), please add data to all fields listed below (find more details information about the fields in the [Azure ADO global work item field specifications](#azure-ado-global-work-item-field-specifications) table):

| **Field name** | **Reference name** | **Guidance** |
| --- | --- | --- |
| Title | "System.Title" | One line description of the work. |
| Area path | "System.AreaPath" | Area path of the producer/requestor. If [creating a new dependency with Service Tree in Dependency Tracker](../../../ExtensionsAndTools/DependencyTracker/create-dependency/create-dependency.md#create-a-new-work-item-with-a-service-tree-service) the area path is set to the ADO area path from Service Tree metadata. |
| Iteration path | "System.IterationPath" | Dependency Tracker sets iteration path to root of the ADO project. |
| Assigned to | "System.AssignedTo" | When creating a dependency using ADO, please set to the identity of the producing team's PM. If [creating a new dependency with Service Tree in Dependency Tracker](../../../ExtensionsAndTools/DependencyTracker/create-dependency/create-dependency.md#create-a-new-work-item-with-a-service-tree-service) the assigned to is set to the Service Tree PM Owner. |
| Description | "System.Description" | Include the description, acceptance criteria, and business impact of the work being requested. If using Dependency Tracker, there is a 250 minimum character requirement to ensure requestors are providing producers clear information. If you are linking work items manually, please ensure there is adequate detail for producing team to triage. |
| Classification | "Custom.Classification" | Check out [the Classification and Sub Classification values](../../WorkItemTypesAndFieldsStandards/classification-and-sub-classification/classification-and-sub-classification.md) to properly classify the producer's work item that is being requested. |
| Sub Classification | "Custom.SubClassification" | Optional to clarify Classification. Check out [the Classification and Sub Classification values](../../WorkItemTypesAndFieldsStandards/classification-and-sub-classification/classification-and-sub-classification.md). |
| Commitment Status | "Custom.CommitmentStatus" | Producer sets Commitment Status based on [this values guidance](#how-do-i-effectively-use-commitment-status-field-values) when [triaging the dependency](../../../ExtensionsAndTools/DependencyTracker/dependency-dashboard/dependency-dashboard.md#triage-dependencies). |
| Commitment Reason | "Custom.CommitmentReason" | Required if Commitment Status is "Rejected" or "Deferred". |
| Target Date | "Microsoft.VSTS.Scheduling.TargetDate" | Requestor sets Target date to the date when the work needs to be completed by. |
| Tags | "System.Tags" | Dependency Tracker sets "PartnerAsk", "Producer", the current semester tag (eg. "Semester:Dt") for producer's work items and "PartnerAsk", "Consumer", and the current semester tag for requestor's work items. If [linking work items manually](../../../ExtensionsAndTools/DependencyTracker/create-dependency/create-dependency.md#manual-dependency-creation-microsoftos-only), please add "Producer" and the current semester tag to the producer's work item and add "Consumer" and the current semester tag to the requestor's work item. |
| Service ID | "Custom.ServiceId" | Service Tree ID of the service responsible for the work. Note: This field is not used for [dependency dashboard grouping](../../../ExtensionsAndTools/DependencyTracker/dependency-dashboard/dependency-dashboard.md#group-by-categorization-mode). |
| Service Name | "Custom.ServiceName" or "AzureOps.ServiceName" | Name of the service responsible for the work.Note: This field is not used for [dependency dashboard grouping](../../../ExtensionsAndTools/DependencyTracker/dependency-dashboard/dependency-dashboard.md#group-by-categorization-mode). |

> [!NOTE]
> If your ADO organization/project does not have the standard fields, please contact <azplanningsup@microsoft.com> so we can help add the fields to ensure dependency creation, triage and reporting to work seamlessly.

## How do I add a Private Preview, Public Preview or General Availability (GA) Date?

Open the work item to update and navigate to the section called Release Schedule (or in some instances just called "Release") then choose a date and save the work item.

![An image with that shows the three fields: Private Preview, Public Preview and GA Dates.](./Release-Schedule.png)

## How do I flag and/or review "Blocked", "At Risk", or "Off Track" work items?

You can update and save the Risk Assessment field in your work items to the "At Risk" or "Off Track" Risk Assessment value.

To review the full set of items that have an "At Risk" or "Off Track" value in the Risk Assessment field you can create a query specific to your area path(s) and then choose the following query filters:

![An image with that shows the three fields: Private, Public and GA Dates.](./at-risk-items.png)

> [!TIP]
> Add details to Risk Assessment Comment field to explain why the work is "At Risk" or "Off Track" to better communicate with partner teams.

## Why don't several work item types have a "Blocked" state?

The "Blocked" state is discouraged since a work item may experience risks during each individual phase of its life cycle. Moving a work item into and out of the same state multiple times creates confusion on how much progress the work item has already made. Tying the blocking action to the Risk Assessment field improves team and planning communication by allowing you to identify where in the process this work item cannot progress. Additionally it assists in identifying an item before it is blocked and allows your team to take action before work can no longer progress.

> [!TIP]
> If you want "blocked" items highlighted on your board, consider defining ["Style Rules"](https://learn.microsoft.com/en-us/azure/devops/boards/boards/customize-cards?view=azure-devops#define-style-rules-to-highlight-cards) that can highlight your work items when the Risk Assessment Field is set to "At Risk" or "Off Track".

## How do I effectively use Commitment Status field values?

The Commitment Status field enables teams to communicate whether the work requested in a dependency ask has been committed to. Dependency producers should triage the dependency and update the Commitment status following [these triage steps](../../../ExtensionsAndTools/DependencyTracker/dependency-dashboard/dependency-dashboard.md#triage).

![A screenshot of the Commitment Status dropdown menu that shows all of the it's field values: "Committed - Current Semester", "Committed - Multi-Semester", "Deferred", "Incomplete", "New", "Rejected", "Under Review".](./Comittment-Status.png)

| **Commitment Status field value** | **Definition** | **Process Details** | **Continuous Planning Notes** |
| --- | --- | --- | --- |
| **New** | The ask that has not yet being reviewed by the producer. | This is the default value of dependencies created by [Dependency Tracker](../../../ExtensionsAndTools/DependencyTracker/dependency-tracker/dependency-tracker.md). | Asks should be triaged monthly |
| **Under Review** | The ask has been acknowledged and taken into review by the producer. | At this stage, clarifying questions should be posed and answered. If the producing team requires more details, the ask should stay in "Under Review" status until the open questions and clarifications are addressed. Ideally, capture the answers within the produced work item itself before the status is updated. | Asks should be in this state for a maximum of one month and then moved to Incomplete, Committed - Current Semester, Committed - Multi-Semester, Deferred or Rejected |
| **Incomplete** | This denotes that the information provided in the dependency is missing critical details that the producer needs to triage the work. | The requestor must provide the additional information that the producer requires so they can determine if they can commit to the work (i.e. clear description, etc.) | Asks should be updated and then producing team to triage once complete |
| **Committed - Current Semester** | Denotes that the ask has been agreed to by the producer within the requestor's requested semester. The work is resourced & delivered in current semester. | The producing team should select this value once they have determined that they will take the item. At this stage, they should ensure that the iteration path is updated by selecting a tighter range of sprint dates instead of leaving it on a semester-level iteration path (e.g. "One\Azure\Selenium" vs. "One\Azure\Selenium\2020-10"). They should also communicate in the work item discussion section any additional details regarding delivery timeline/estimates. | Asks should include a Private, Public or GA Date that is reviewed monthly |
| **Committed - Multi-Semester** | Denotes that the ask has been agreed to by the producer, but the work effort is large and delivery would be over multiple semesters. | The producer should select this value once they have determined that the effort is larger than a semester. **Process:** If "Committed - Multi-semester" is chosen, the producer should **convert the Dependency Feature/Deliverable into an Epic**, add work delivered in current semester and if known, add Features that will be planned for future semester. The iteration path of Epic should be set to the future semester and iteration path for Features should be set to the respective semesters where work will be delivered. The producer should also communicate in the discussion section any additional details regarding delivery timeline/estimates. | Asks should include a Private, Public or GA Date that is reviewed monthly |
| **Rejected** | Denotes that the ask has been declined by the producer because it is invalid. | An ask that does not meet the criteria of an engineering dependency (i.e. bug fix request which should be filed as a Bug work item type). | If an ask has been rejected by the producing team, that same ask should not be submitted again unless producing team requests it at a future date |
| **Deferred** | The ask is understood and accepted as a valid ask, but the producer cannot commit to it at that time but will consider committing to it in a future iteration. | The producer will revisit "Deferred" items at a future date. Requestors should take this as a flag that their request will *not* be addressed in the semester they requested. | This ask can be resubmitted by consuming team (assuming it is still a valid ask) again the following quarter |

## How do I leverage values in the Status Field?

The Status field enables teams to accurately track a deliverable (Epic/Feature) through a consistent set of delivery milestones/steps.

### Key Benefits

- Enhanced Transparency: Delivery status is reported clearly to stakeholders
- Improved-Decision Making: Accurate delivery status enables improved strategic planning and resource allocation
- Better Collaboration: Clear reporting facilitates smoother interactions within upstream and downstream partner teams
- Increased Efficiency: Streamlined reporting reduces time spent in meetings

### Status Field Values

| **Status Field Value** | **Definition** |
| --- | --- |
| **Not Started** | Work for the product/feature has not started. The feature is available in the backlog |
| **Feasibility Study** | Proposal, strategy analysis and justification specs for the features are in progress |
| **Design Phase** | The design of the deliverable is in progress. Technical design document is the final result of this phase |
| **Coding** | Design work is complete and coding is in progress |
| **Code Complete** | Coding for all associated dependencies of the deliverable is complete |
| **Test Signed-Off** | All quality gates and validations complete |
| **In Canary** | Deployment to Canary |
| **Delivery Stage - Internal Release** | Delivered for internal release to partners, with fast feedback loop |
| **Delivery Stage - Private Preview** | Early access to feature/s for a limited group of customers |
| **Delivery Stage - Public Preview** | Early access to feature/s for a broader group of customers |
| **Delivery Stage - GA** | Delivered in production for all customers |

[!INCLUDE [Footer](../../../_templates/_footer/_footer.md)]
