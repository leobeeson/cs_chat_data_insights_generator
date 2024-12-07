# Conversation Enrichments Schema Fields

* **Journey Phase**: `phase`
  * Type: `list[Enum[str]]`
  * Deductively valid or inductively very strong customer journey **Phases** inferred from the chat conversation identifying where the user is on the customer journey, or that he has gone through before reaching the current phase where he finds himself.
* **Journey Touchpoint**: `touchpoint`
  * Type: `list[Enum[str]]`
  * Deductively valid or inductively very strong customer journey **Touchpoint** inferred from the chat conversation identifying which actions or events the user is interacting with right now, or has interacted with so far along the customer journey.
* **Journey Problem**: `problem`
  * Type: `list[Enum[str]]`
  * Deductively valid or inductively very strong customer journey **Problems** inferred from the chat conversation identifying which problems, frictions, or barriers the user is experiencing or has experienced so far along the customer journey.
* **Emotion**: `emotion`
  * Type: `list[Enum[str]]`
  * Deductively valid or inductively very strong customer journey **Emotions** inferred from the chat conversation identifying which emotions the user is feeling or has felt so far along the customer journey.
* **Cognitive State**: `cognition`
  * Type: `list[Enum[str]]`
  * Deductively valid or inductively very strong customer journey **Cognitive State** inferred from the chat conversation identifying which mental or cognitive states the user is experiencing or has experienced so far along the customer journey.
* **CS Analysis**:
  * Type: `str`
  * Detailed decomposition of customer journey phases, actions, events, problems, frictions, barriers identified from the chat conversation.
  * Critical analysis from a Customer Service perspective of the interactions between the customer and customer service agent.
  * Practical insights from a Customer Service perspective extracted from the interactions between the customer and customer service agent.
* **Dropped Off**: `dropped_off`
  * Type: `bool`
  * Whether the customer dropped off the chat conversation abruptly or prematurely.
  * You can tell by the human user attempting to resolve the issue, but the customer not responding or providing feedback.
* **First Call**:
  * Type: `bool | None`
  * Whether the chat conversation was the customer's first time reaching out to Customer Service for resolving the issue.
  * `None` if uncertain.
* **Resolved**:
  * Type: `bool`
  * Whether the customer's issue was resolved in the chat conversation.
  * Infer the customer's issue resolution either from customer confirmation of inferring from the conversation outcome.
  * If uncertain, return `False`.
* **Resolver**:
  * Type: `Enum[str] | None`
  * If customer's issue was resolved, indicates whether the customer's issue was resolved by a bot or human agent.
  * `None` if issue unresolved.
* **Customer Effort Score**:
  * Type: `int | None`
  * Integer between 1 and 5 indicating the customer's effort exerted trying to resolve their issue.
  * 1 is low effort, 5 is high effort.
  * Infer the customer's effort score either from customer confirmation of inferring from the conversation outcome, whether issue was resolved or not.
* **Net Promoter Score**:
  * Type: `int | None`
  * Integer between 1 and 10 indicating the customer's likelihood to recommend the company to others.
  * 1 is low likelihood, 10 is high likelihood.
  * Infer the customer's NPS either from customer's explicitly provided NPS score, or if missing, infer it from the conversation outcome and service quality.
* **Agent Reliability Score**:
  * Type: `int | None`
  * Integer between 1 and 10 indicating the human agent's ability to perform the promised service dependably and accurately.
  * 1 is low reliability, 10 is high reliability.
  * None if no human agent was involved.
* **Agent Assurance Score**:
  * Type: `int | None`
  * Integer between 1 and 10 indicating the human agent's ability to convey trust and confidence to the customer.
  * 1 is low assurance, 10 is high assurance.
  * None if no human agent was involved.
* **Agent Empathy Score**:
  * Type: `int | None`
  * Integer between 1 and 10 indicating the human agent's ability to understand and and provide caring, individualized attention to customers.
  * 1 is low empathy, 10 is high empathy.
  * None if no human agent was involved.
