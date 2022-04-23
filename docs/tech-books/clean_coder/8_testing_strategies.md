# 8. Testing Strategies



## QA should fine nothing

- QA is part of team



## The test automation pyramid

![8 Testing Strategies - Tips from The Clean Coder - DEV Community](https://res.cloudinary.com/practicaldev/image/fetch/s--QVYSGuqi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://3.bp.blogspot.com/-EeP4wxpaeKM/TzN5fOnavyI/AAAAAAAAABM/Z4b-Udt-n30/s1600/ATPyramid.png)



### Unit tests

- By programmer sfor programmers
- Run on CI
- Close to 100% coverage



### Component tests

- Paasess input data to component and gahters output data
- These are Acceptance tests
- Check if input match output
- Written by QA and Business
- Coverage: Roughly half of system
- Mostly check happy path situations



### integration tests

- For larger systems
- Written by lead architect or designers of system
- Check architecture of system is ound
- Not part of CI



### System Tests

- Run against entire system
- Writen by architects and leads



### Manual exploratory tests

- Goal is not coverage
- Ensure runs wells with human operation



