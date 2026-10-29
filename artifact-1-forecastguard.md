# Artifact 1: ForecastGuard – Project Cost Risk Assistant

## Project Overview

ForecastGuard is an AI assistant I developed during the AI Lab activity in Machine Learning Fundamentals. The purpose of the assistant is to support Project Controls Analysts by identifying potential forecast risks before they become cost overruns.

The assistant reviews project information such as actual costs, accruals, commitments, Estimate to Complete, Estimate at Completion, physical progress, productivity, schedule exposure, and remaining scope.

## Problem

In project cost analysis, financial data does not always tell the full story. Actual costs may be posted in a different month from when the work was performed. Open purchase order balances may also be different from the amount that will actually be spent.

Another important issue is that a project may appear healthy because actual costs are below budget while the forecast continues to increase. For this reason, I wanted to build an assistant that focused on early warning indicators instead of only current spending.

## AI Tools Explored

Before developing ForecastGuard, I explored several AI tools during the AI Lab.

- Claude was used to test general chatbot responses and consistency.
- Cost Analyst Pro was used to explore project cost review processes and forecast risk analysis.
- STORM was used as a research assistant to organize information and identify supporting concepts related to project controls and forecasting.

These tools helped me compare different AI capabilities and understand how specialized instructions can improve the quality of responses.

## Design and Development

I selected Chatbase to build ForecastGuard because it allowed me to create a specialized assistant, define detailed instructions, test different scenarios, and share the final assistant through a public link.

The assistant was instructed to distinguish between:

- Current financial position
- Accounting timing differences
- Contractual commitments
- Forecast exposure
- Potential project risks

The assistant was also instructed not to invent missing information and to separate facts, risks, assumptions, recommended actions, project health, and forecast confidence.

## Testing and Iteration

I tested ForecastGuard using four project cost scenarios.

### Test 1: Healthy Project

The first scenario represented a financially healthy project.

The initial version rated the project Yellow even though there were no specific adverse cost trends. I determined that the assistant was treating missing information as project risk.

I updated the instructions so that Project Cost Health and Forecast Confidence would be evaluated separately.

After the change, the assistant correctly rated the project Green while maintaining Medium Forecast Confidence.

This was the most important improvement during the testing process because it demonstrated how AI responses can improve through tuning and iteration.

### Test 2: Late Invoice and Cost Timing

The second scenario included a $250,000 invoice posted in October for work that was completed and accrued in September.

ForecastGuard correctly identified the invoice as a timing difference rather than a new October cost increase. It also identified the need to confirm that the prior accrual was reversed to avoid double counting.

### Test 3: Open Purchase Order Balance

The third scenario tested whether ForecastGuard would automatically treat an open purchase order balance as future spend.

The purchase order had a $400,000 open balance, but only approximately $150,000 of remaining work was expected, plus a $75,000 pending change.

ForecastGuard correctly determined that the full $400,000 should not automatically be included in the forecast. It calculated an indicative remaining cost of approximately $225,000, subject to validation.

### Test 4: Forecast Deterioration

The final scenario tested whether the assistant could identify a project that appeared favorable based on actual spending but had a deteriorating forecast.

The EAC increased from $9.65 million to $10.55 million over three months. Mechanical productivity was declining, additional subcontract quantities were expected, and a possible schedule extension was being discussed.

ForecastGuard rated the project Red and correctly explained that lower actual spending did not represent favorable performance because the forecast and operating indicators showed increasing risk.

## Results

The final assistant demonstrated the ability to:

- Identify forecast risk trends
- Distinguish timing differences from actual cost growth
- Challenge open commitments
- Evaluate ETC and EAC assumptions
- Identify productivity and schedule exposure
- Separate project health from forecast confidence
- Recommend practical management actions

## Lessons Learned

This project helped me understand that AI systems should not be accepted only because their responses appear professional or reasonable.

The most important part of the project was testing the assistant against real project controls situations and using professional knowledge to determine whether the responses were correct.

The first test showed that even a well designed AI assistant can produce a reasonable sounding but incorrect conclusion. By adjusting the instructions and testing the assistant again, I was able to improve its decision logic.

This experience demonstrated the importance of domain knowledge, validation, testing, and iteration when developing AI solutions.

## Live Project

ForecastGuard – Project Cost Risk Assistant:

https://www.chatbase.co/preview/CYWHw-PCA4BgGLcGsZg_C?channel=chat-widget
