#### Scan Project with DLP (Data Loss Prevention)

* How to scan and protect project with sensitive information using Automatic DLP 
   * Navigate to Security -> Data Loss Prevention -> Enable API
   * Create Configuration -> Select resource to scan <br>
   _(note): You can scan at the organisational level assuming there are a bunch of files you need to scan through._
   *  Under manage schedules, specify filters, frequency and conditions to what and when to scan.
   * Select inspection template to specify the types of sensitive data to scan.
     * Create a new one
     * MANAGE INFOTYPES shows what you want to inspect
     * Inspection Ruleset lets you exclude or include additional findings.
     * Set confidence threshold to a likelihood of possible.
     * Manage service agent container & billing-> create a new project as a service agent
     * Set resource location `in same location as your data`
     * create

    **_This scan runs automatically in respects to schedule specified._**

