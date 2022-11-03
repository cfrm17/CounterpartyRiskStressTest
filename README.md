# Counterparty Risk Stress Test

Stress testing is simulating an exceptional but plausible economic scenario to identify key risks to the bank and to gain assurance the bank is sufficiently well capitalized to withstand such scenarios.

Whilst ‘stressed’ counterparty exposure profiles are used for regulatory capital calculations under Basel III, there is a key difference to genuine stress testing. The Basel III stressed scenario is simply calibrated to a historical time of stress so can only simulate the effect of history repeating itself, whilst stress testing should seek to conceive of potential scenarios that have never happened historically, but could potentially happen in the future. 

A critical element of this will be identifying potential dependencies between market factors that may not be observed in historical correlations. For example, a historical correlation analysis of USDCAD and Canadian government credit spreads would likely observe minimal correlation, but it is reasonable to expect that in a scenario where Canadian government spreads were to widen significantly, that CAD would weaken as a result. There are two types of credit spreads: CDS spread and bond spread. See https://finpricing.com/lib/FiBondCoupon.html

Stress testing can be applied to any of the market data inputs to the counterparty credit risk (CCR) simulation:
·         Initial market data (either a single factor or multiple factors)
·         Parameters for evolution of future market data (e.g. mean reversion and drift)
·         Correlations between market factors

For CCR, it is desirable that stress scenarios are designed to as a coherent scenario, reflecting the correlations and dependencies that can be foreseen between market factors under specific economic outcomes. This is due to the increased importance of right and wrong way risk within CCR.

In the context where Stress tests are based on exceptional but possible scenarios, the origin of a stress scenario is the economics department. It then gets transmitted to the Stress Test group for translation into market factor shocks that CCR models can interpret. At this point, calibration takes place: stressed market data and historical prices are taken as input to that process; it yields stressed parameters (recall kappa, sigma and theta from before) which are then passed on the CCR engine where EE, PFE are calculated for each portfolio. Depending on the current application, whether it is used for ICAAP or regulatory stress tests, the results are compiled and sent to the relevant team.

CCR stress test results can be more difficult to interpret than market risk VaR – there is no single 95th percentile loss to focus on, but instead we must consider the impact on the individual exposures to thousands of different counterparties. We can make this this more manageable by for example focusing on the top 50 counterparties, or aggregating by country or industry sector.

An alternative interpretation is to look at the effect on counterparty risk capital requirements in the stressed scenario, to identify scenarios that cause the greatest increase in capital requirements.

We can also use CCR stress tests to identify liquidity risks due to large collateral postings requirements. This can be an issue where we have significant risk positions against uncollateralized counterparties, hedged in the interbank market or through central counterparties. As we simulate the collateral balance to be posted to counterparties along each path, we can determine the 95th percentile largest net collateral outflow in a particular stress scenario.

Key requirement within Basel III for counterparty risk stress testing include:
·         Stress of principal market risk factors at least monthly to identify directional concentrations
·         Multifactor stress testing of severe economic scenarios and stress testing of non-directional risk factors (curve, basis etc.) at least quarterly
·         Stress testing of the joint movement of exposures and counterparty creditworthiness at least quarterly.
