# The story so far

## Forcing perturbation

**Main experiment: UP and DOWN**

Increase (UP) and decrease (DOWN) the winds (both u and v components) near Antarctica by 10%. Only the winds south of the dividing line between the annual average easterly and westerly winds from the JRA55-9091 winds are perturbed. This is done by selecting a line following the minimum in the absolute value of the annual average wind speed. We add/subtract 10% of the rolling monthly mean u and v wind velocities to the original JRA55 u and v winds. By using the rolling monthly mean, we ensure that we're not amplifying the storm activity, and also minimising change to the seasonal cycle. For example, the easterlies in the control are strong in winter and weak in summer, so if we were to add/subtract a constant fraction of the annual wind speed (rather than monthly wind as we do here), we would inadvertently be overly strengthening the summer winds compared to the winter winds.

We chose to perturb both the u and v components of the wind speed, because in many places the wind follows the topography of the Antarctic continent, so the meridional component of the wind is really just a deflection of the easterlies by Antarctic topography. Therefore we thought it seemed to make most sense to change both components. This means, however, that the experiment cannot be understood purely as an 'easterlies' experiment.

**Addtitional experiment: UP, but no perturbed katabatics in DSW formation regions**

We did a second experiment which is exaclty the same as the UP case from the main experiment, but we omit the wind increase in the four DSW formation regions (Ross Sea, Adelie Land, Prydz Bay, Weddell Sea). Instead, these regions are subject to the control winds. The experiment aims to test if the increase in DSW formation in the UP case is driven by the changed katabatics, i.e. is a local process.

**Ideas for further experiments:** (Note that we prefer to make use of the existing experiments.)
  * Reversal of the katabatics experiment, i.e. we only increase the winds in the DSW formation regions. We don't expect much of a change compared to the control run though.
  * Changing only the 'along-slope' winds. Implementation might be challenging. Motivation for this experiment: this was the initial idea of the project, the current implementation in UP does also increase meridional winds.
  * ...?

### Comparison with reanalysis trends/CMIP6

To do: What are the easterly trends in reanalysis (overview of Hazel et al. 2019 and Julia's analysis)? How do the CMIP6 models compare with reanalysis over the historical period (i.e. how much do we trust them) and what are the easterly projections in the future?

**Historical period (1958 - 2015) mean wind fields:**
  * [JRA55-do has stronger winds than CMIP6 multimodel mean](https://github.com/adele157/easterlies-collaborative-project/issues/12#issuecomment-897213042), particularly the meridional winds 

**Historical period (1958 - 2015) wind trends:**
 *  [Zonal wind trends](https://github.com/adele157/easterlies-collaborative-project/issues/12#issuecomment-897213042) in JRA55 show the southwards shift of the westerlies *and intensification of the easterlies in some coastal regions*. These regions are adjacent to DSW formation sites. CMIP6 multimodel mean only captures the westerly trends, none of the more localized regions of intensification, and neither do the individual models.
 *  [Meridional wind trends](https://github.com/adele157/easterlies-collaborative-project/issues/12#issuecomment-897213042) in JRA55-do show an increase of the off-shore winds in the western Weddell, Prydz Bay and Ross Seas. And a decrease of the off-shore winds in East Antarctica and East Ant. Peninsula. Of these, only the latter is present in CMIP6 multimodel mean. None of the individual models capture these trends either.

**Projected changes (end of 22nd century):**

[Projected changes in zonal and meridional winds](https://github.com/adele157/easterlies-collaborative-project/issues/12#issuecomment-897282904) show:

  * The southward shift of the westerlies, affecting mostly the Antarctic Peninsula and East Antarctica.
  * Decrease of the off-shore winds in some regions (western Ross Sea, eastern Antarctic Peninsula, Amundsen Bellinghausen Seas) and increase in others (eastern Ross Sea, a portion of the Weddell, and Prydz Bay)

## Simulation responses

Changes here are described for the UP perturbation, and unless otherwise specified, changes are largely symmetric for the UP and DOWN perturbations.

  * DSW formation increases (Evidence: [bottom age decreases](https://github.com/adele157/easterlies-collaborative-project/issues/11#issuecomment-880288513) following bottom water pathways, [abyssal cooling](https://github.com/adele157/easterlies-collaborative-project/issues/4#issuecomment-875259285) throughout the Southern Ocean,  [overflow velocities increase](https://github.com/adele157/easterlies-collaborative-project/issues/7#issuecomment-876866344), [sea ice formation increases](https://github.com/adele157/easterlies-collaborative-project/issues/10#issuecomment-877990121) etc).
  
  * The increase in the lower cell overturning is associated with an increase in the upward heat flux from the abyss to the surface. This impacts temperature and salinity on the shelf as follows: [SST warms, SSS salinifies, bottom salinity increases in DSW formation regions, bottom temperature cools in DSW formation regions](https://github.com/adele157/easterlies-collaborative-project/issues/4#issuecomment-875259285), and the [shelf regions directly downstream of DSW formation sites warm at the bottom](https://github.com/adele157/easterlies-collaborative-project/issues/16#issuecomment-884591714) due to less along-shelf connectivity from cold upstream waters.
  
  * The [ASC strengthens at depth downstream of DSW formation sites](https://github.com/adele157/easterlies-collaborative-project/issues/7#issuecomment-876146351).
  
  * [Sea ice thickness/concentration generally decreases](https://github.com/adele157/easterlies-collaborative-project/issues/10#issuecomment-875248868) (except in the NE Weddell Sea and in the open ocean off the Amundsen). Is this due to more northerly ice advection, or SST warming?
  
  * [Mixed layers deepen](https://github.com/adele157/easterlies-collaborative-project/issues/14#issuecomment-877979016) in response to more wind-driven mixing in summer and more shelf convection in winter.
  
  * A fast Ekman response is seen in the first year: [SSH increases over the shelf](https://github.com/adele157/easterlies-collaborative-project/issues/23#issuecomment-893299741), and [SST cools](https://github.com/adele157/easterlies-collaborative-project/issues/4#issuecomment-880263337). However these responses are quickly overwhelmed with changes in the opposite direction driven by the increasing DSW.
  
  * To do: Add notes on Ekman pumping, sections of shelf that cool at the bottom (e.g. Amundsen).

Why is DSW increasing? (Hypotheses)

  * <del>Local katabatics: The difference in DSW formation between the normal UP experiment and the UP experiment without perturbed katabatics is minimal, which suggests that it is **not** the local change in the katabatics driving the increase in DSW formation. 

  * Wind-driven Ekman upwelling: Winds drive [large-scale Ekman upwelling](https://github.com/adele157/easterlies-collaborative-project/issues/20) and the signal propagates down the isopycnals, i.e. different (warmer) water is upwelled as denser isoycnals outcrop on the continental shelf. Due to the larger heat availability more more DSW/sea ice can be formed. An idea to test this hypothesis is to look at the start of the model run befre the first DSW formation season to identify the rise of isopycnals.

  * Increased sea ice advection offshore: Instead of a local advection of sea ice by the katabatics in the DSW formation regions, it's the [large-scale offshore advection of sea ice](https://github.com/adele157/easterlies-collaborative-project/issues/10) which creates more ice-free area and allowing for more DSW formation. Ideas to better understand this hypothesis is to look at sea ice transport across, e.g., the 1000-m isobath.

  * Above mechanisms don't exclude each other.
