using OpenQA.Selenium;
using OpenQA.Selenium.Support.UI;

public class SeleniumAssist
{
    public readonly string HOMEPAGEURL = "https://localhost:8080";

    public ApplicationDbContext Context { get; }
    public IWebDriver Driver { get; }

    public SeleniumAssist(IWebDriver driver)
    {
        Driver = driver;
    }

    public void TestUrl(string url = "") =>
        Driver.Navigate().GoToUrl($"{HOMEPAGEURL}{url}");

    public void ClickElementById(string id) =>
        Driver.FindElement(By.Id($"{id}")).Click();

    public void SendKeysToTextBoxById(string elementId, string keys) =>
        Driver.FindElement(By.Id($"{elementId}")).SendKeys(keys);

    public IWebElement FindElementById(string id) =>
        Driver.FindElement(By.Id(id));

    public IWebElement FindElementByValue(string value) =>
        Driver.FindElement(By.XPath($"//*[contains(text(), '{value}')]"));

    public bool GetUrlEquals(string url) =>
        Driver.Url.Equals(url);

    public void SelectElementFromDropDownList(string dropDownId, string selectText) =>
        new SelectElement(Driver.FindElement(By.Id(dropDownId))).SelectByText(selectText);
}
