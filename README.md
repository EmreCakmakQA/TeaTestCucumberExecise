# Passionate Tea Test Selenium/Cucumber Execise

The aim of this repo is to demonstrate the use of cucumber and selenium. The task is to automate front end testing of a demo site.

## Task

Write a test for the following case scenario:

```
Feature: Shopping on a website 
As a person 
I want to browse items on a website 
So that I can purchase the items I want 

Scenario: Browse the items available on the website 
Given the correct web address 
When I navigate to the 'Menu' page 
Then I can browse a list of the available products. 

Scenario: Add an item to the checkout 
Given the correct web address 
When I click the checkout button 
Then I am taken to the checkout page 

```
The *Given, When, Then* syntax makes it great for styling off of a Jira board and incorporating user stories.

In this task, the "*Given that, When*" is written as follows:

```
    @Given("^the correct web address$")
	public void the_correct_web_address() {
		driver.get(URL);
		assertEquals("Welcome", driver.getTitle());

	}

	@When("^I navigate to the 'Menu' page$")
	public void i_navigate_to_the_Menu_page() {
		driver.findElement(By.linkText("Menu")).click();
	}

	@Then("^I can browse a list of the available products\\.$")
	public void i_can_browse_a_list_of_the_available_products() {
		assertThat(driver.findElement(By.cssSelector("#wsb-element-00000000-0000-0000-0000-000453230000 strong")).getText(), is("Green Tea"));
	    assertThat(driver.findElement(By.cssSelector("#wsb-element-00000000-0000-0000-0000-000453231072 strong")).getText(), is("Red Tea"));
	}

```

This allows for incorporation of Behaviour Driven Development.




