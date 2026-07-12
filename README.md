              waeaving-Hand-Lab-Mama-Nkechi
  Complete the 5 Whys table to identify the root cause of the security failure and then rewrite your fix to explain how the system would alert a user on a basic phone via SMS or USSD.

  1. Why did Mama Nkechi lose ₦45,000?
--  Because two large transactions were sent to Lagos from her account.
2.Why were those transactions allowed?
--Because the security system did not recognize the transactions as unauthorized
3.Why didn't the system alert her?
--Because the fraud detection rules were not sensitive to geographic or behavioral anomalies
4.Why wasn't the location change detected?
--Because the system was designed to focus only on transaction volume rather than user location context
5.Why (ROOT CAUSE)?
--The system design prioritized high-volume throughput over local context-aware security, failing to account for the specific behavioral patterns of rural market traders


                  What to do on the "5 Whys" (Advice)
To effectively use the "5 Whys" technique for your assignments and professional work, follow these three steps:

1. Dig for the System, Not the Person
As noted in your text: "Blame the system, not the person. People operate within systems. Fix the system." When performing your 5 Whys, if your answer points to a person (e.g., "Mama Nkechi didn't check her phone"), stop. Rephrase the question to look at the process. Instead, ask: "Why did the system allow a massive transaction to pass without a secondary confirmation mechanism that would reach her, regardless of her phone usage?"

2. Stop at the Actionable Root Cause
The goal of the 5th "Why" is to find a point where you can actually make a change. If your 5th "Why" is something vague like "The world is unfair," you have gone too far into philosophy. If your 5th "Why" identifies a specific policy, design oversight, or missing technical feature (like the missing "location-change alert"), you have reached a productive root cause that you can fix.

3. Test the "Therefore" Path
Once you have your chain of 5 Whys, read them backwards using "therefore":

The system lacked context-aware security; therefore, it failed to detect the location change; therefore, it did not trigger an alert; therefore, the fraud went through; therefore, Mama Nkechi lost her money.

If the "therefore" logic flows perfectly, you have found a solid causal chain.
Data structure sketch – Show how the transaction data is stored (e.g., as a table/CSV, dictionary, or list). A table is the most appropriate because it preserves all transaction details.
Date	Time	Amount (₦)	Type	Location
Jun 1	10:03	+15,000	Receive	Market
Jun 1	14:22	-2,000	Send	Market
Jun 2	09:17	+8,500	Receive	Market
Jun 3	11:45	-45,000	Send	Lagos
Jun 3	11:47	-5,000	Send	Lagos

Why this structure?
A table efficiently stores multiple transactions, keeps all fields together, and makes it easy to compare dates, locations, and amounts to detect suspicious behaviour.

Fraud pattern sentence – Complete the sentence from the lab.

This looks like fraud because normally Mama Nkechi receives payments and only makes small local transfers at the market, but on June 3 she suddenly made two large outgoing transfers from Lagos within two minutes, which is unusual behaviour.

Complete the 5 Whys analysis – This was specifically identified as missing.
Question	Answer
1. Why did Mama Nkechi lose ₦45,000?	Because unauthorized transfers of ₦45,000 and ₦5,000 were processed from her account.
2. Why were those transactions allowed?	Because the system did not require a secondary verification for a large transfer from an unusual location.
3. Why didn't the system alert her?	Because its fraud detection rules did not identify the sudden change in transaction behaviour.
4. Why wasn't the location change detected?	Because the system did not compare the transaction location with Mama Nkechi's normal transaction history.
5. Why (Root Cause)?	The mobile money system lacked simple risk-based security checks, such as detecting unusual locations or requiring confirmation for large, abnormal transactions.
A practical one-sentence fix – Your instructor said your AI solution is too abstract. The fix should suit a low-bandwidth, offline-friendly environment.

A suitable answer is:

If a large transfer is attempted from a new location, the system should send a USSD or SMS confirmation request and only complete the transaction after the user enters a verification PIN.

This solution works on basic mobile phones without requiring internet access or advanced AI
