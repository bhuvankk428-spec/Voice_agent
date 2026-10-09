# Home Credit LAP Qualification Voice Agent

An AI-powered voice agent built with **Retell AI** to conduct
preliminary eligibility checks for a Home Credit Loan Against Property
(LAP) offer of up to **₹75,00,000 (₹75 lakh)**.

## Live Demo

**Try the Retell AI agent:**\
[Open the Home Credit LAP Voice Agent
Demo](https://agent.retellai.com/orb/agent_2b3c09785d9888b1ca3f9981e3?token=908c53630479ceea65aa9574161411c7)

> Note: This is a shareable testing link. Confirm that it is intended
> for public sharing before publishing it. Do not publish private API
> keys, credentials, or real customer information.

## Project Overview

The agent speaks with a customer, explains the purpose of the call, and
checks preliminary eligibility using a defined set of business rules. It
handles customer responses in natural language, remembers details
already provided, asks for missing information, and routes certain
existing-loan requests to a specialist.

The agent performs a **preliminary eligibility check only**. It does not
approve or guarantee a loan.

## Key Features

-   Outbound-style introduction explaining the company and purpose of
    the call.
-   Customer identity confirmation and busy-customer callback handling.
-   Seven-step preliminary eligibility checklist.
-   Captures information supplied out of order and avoids repeating
    answered questions.
-   Handles corrections by using the customer's latest clear answer.
-   Detects disqualifying conditions and ends the fresh-loan flow
    appropriately.
-   Routes existing-loan transfer, balance-transfer, refinancing, and
    EMI-reduction requests to a loan-transfer specialist.
-   Responds to common company and loan questions using approved
    knowledge-base information.
-   Avoids inventing interest rates, fees, approval guarantees, or
    unsupported product terms.
-   Post-call extraction of customer and eligibility details.

## Eligibility Rules

  -----------------------------------------------------------------------
  Check                               Rule
  ----------------------------------- -----------------------------------
  Property type                       Residential, commercial, and
                                      industrial properties can proceed.
                                      Agricultural property is not
                                      eligible under this assignment's
                                      rules.

  Ownership                           Sole or joint ownership can
                                      proceed.

  Original property documents         Originals must be available for
                                      verification.

  Requested loan amount               Maximum ₹75,00,000. If the customer
                                      requests more, the agent offers the
                                      ₹75 lakh cap and asks whether they
                                      wish to proceed.

  Occupation                          Salaried or self-employed.

  Income mode                         Income must be received through a
                                      bank/banking channel. Cash income
                                      does not meet the assignment's
                                      criteria.

  Property market value               The agent records the customer's
                                      estimate. No minimum threshold is
                                      specified in the assignment rules.

  Repayment tenure                    Between 3 and 15 years, inclusive.
  -----------------------------------------------------------------------

### Existing Loan Requests

If a customer wants to transfer or refinance an existing property loan,
complete a balance transfer, or reduce an existing EMI, the agent stops
the fresh-loan qualification and directs the customer to a loan-transfer
specialist. An existing loan alone should not trigger this route if the
customer is asking for an additional new loan.

## Conversation Flow

1.  Confirm the intended customer's identity.
2.  Introduce Home Credit and explain the LAP offer and reason for
    calling.
3.  Confirm that the customer has time to continue.
4.  Check whether the customer needs a new loan or help with an
    existing-loan transfer/EMI reduction.
5.  Collect the seven eligibility items, skipping details already
    clearly provided.
6.  Apply disqualification or specialist-routing rules when relevant.
7.  If all required checks pass, explain that a senior loan expert will
    contact the customer to discuss next steps and exact interest-rate
    details.
8.  Record the conversation transcript and post-call extraction results
    where supported by the platform.

## Technology

-   **Retell AI** --- voice-agent configuration, conversation handling,
    testing, and call analysis.
-   **Knowledge Base** --- approved company information and frequently
    asked questions.
-   **Post-call extraction** --- structured capture of customer and
    eligibility details.

## Post-Call Data

The agent is configured to extract these fields:

-   `customer_verified`
-   `property_type`
-   `ownership_status`
-   `documents_available`
-   `loan_amount`
-   `occupation`
-   `income_mode`
-   `market_value`
-   `tenure_years`
-   `final_outcome`
-   `disqualification_reason`
-   `callback_time`

The actual fields and results depend on the saved Retell configuration
and the information stated during each call.

## Example Eligible Scenario

A fictional customer: - Has a residential property. - Jointly owns the
property. - Has the original property documents available. - Requests
₹50 lakh. - Is salaried and receives income through a bank. - Estimates
the property's market value at ₹1 crore. - Prefers a 10-year repayment
tenure.

Under the assignment's preliminary rules, the agent can complete the
checklist and tell the customer that a senior loan expert will contact
them. This is not a loan approval.

## Limitations and Responsible Use

-   This is a demonstration project for preliminary qualification, not
    an automated loan approval system.
-   Final eligibility and approval are determined by the lender's
    assessment.
-   Exact interest rates, fees, processing times, and other product
    terms must come from approved company information or a qualified
    representative.
-   Do not use real customer personal or financial information in public
    demonstrations.
-   Public access to the demo depends on the Retell link and its sharing
    settings.

## Repository Contents

Suggested repository structure:

``` text
home-credit-lap-voice-agent/
├── README.md
├── docs/
│   ├── agent-prompt.md
│   ├── eligibility-rules.md
│   └── demo-evidence.md
└── assets/
    └── screenshots/
```

Add only files you are allowed to share. Do not upload API keys, access
tokens other than an intentionally public demo link, private recordings,
or customer data.

## Demo Evidence

For an assignment submission, include evidence you are permitted to
share:

-   Public Retell testing link.
-   Screenshot of the agent configuration.
-   Screenshot of the attached Knowledge Base.
-   Screenshot of post-call extraction configuration.
-   Call transcript and audio/recording links for demonstration
    scenarios, if required.
-   Screenshots or notes showing the extracted fields and final call
    outcomes.

Make sure all evidence links are accessible to the evaluator.

## Author

**Bhuvan K. K.**

Project: Home Credit Loan Against Property Qualification Voice Agent\
Platform: Retell AI
