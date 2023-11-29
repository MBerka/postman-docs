---
title: "Configure API Governance rules in Postman"
updated: 2023-03-06
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "API Security and Governance Part 1: Automating Governance"
    url: "https://youtu.be/rdMAKc-_NIw"
  - type: link
    name: "API Security and Governance Part 2: Customizing Governance with Spectral Rulesets"
    url: "https://youtu.be/TDOuZcKQId4"
  - type: link
    name: "Set Up Enterprise-Wide API Governance with .NET Core + Spectral | Postman Enterprise"
    url: "https://youtu.be/2zLoW_p0OFQ"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "Big improvements to Postman API Governance"
    url: "https://blog.postman.com/api-governance-improvements/"
---

> [Configurable governance rules are available on Postman Enterprise plans.](https://www.postman.com/pricing) If you don't have an Enterprise account, you'll be able to see the API Governance page, but you won't be able to turn rules on or off or add new rules.

You can customize the API Governance rules that Postman applies to your [API definitions](/docs/api-governance/api-definition/api-definition-warnings/). Adhering to these API Governance rules at the start of the API lifecycle keeps your API consistent without requiring extra work at later stages. This can prevent unnecessary delays for your organization.

[Super Admins](/docs/collaborating-in-postman/roles-and-permissions/#team-roles) and [API Governance Managers](/docs/collaborating-in-postman/roles-and-permissions/#team-roles) can configure rules and turn them on and off for workspaces within your team.

<img alt="API governance dashboard" src="https://assets.postman.com/postman-docs/v10/api-governance-dashboard-v10.jpg"/> <!-- TODO: update screenshot -->

## Contents

* [Accessing the configurable API Governance rules](#accessing-the-configurable-api-governance-rules)
* [Adding rules to your API Governance configuration](#adding-rules-to-your-api-governance-configuration)
    * [Importing rules from the rule library](#importing-rules-from-the-rule-library)
    * [Adding custom rules](#adding-custom-rules)
* [Turning configured rules on and off](#turning-configured-rules-on-and-off)
* [Editing custom rules](#editing-custom-rules)
* [Testing custom rules](#testing-custom-rules)
* [Removing rules from your API Governance configuration](#removing-rules-from-your-api-governance-configuration)

## Accessing the configurable API Governance rules

1. Go to the [Postman home screen](https://go.postman.co/).
1. Select **API Governance** from the team information pane.

## Adding rules to your API Governance configuration

In addition to the rules turned on by default in Postman, you can add other rules to your team's rule library from the rule library. You can also create your own custom rules for API definitions in OpenAPI format.

### Importing rules from the rule library

The rule library has Postman's API governance guidelines, Zalando's RESTful API and event guidelines, and Postman's OWASP API guidelines.

1. Select the **Rule Library** tab, and then select the **Rules** tab.
1. Select **Import** to open the rule library.
1. Select **Import** next to a rule to import it. Details and API format requirements are available under the rule name.

    > You can select **View all** below a set of guidelines to view all of its rules. To import all rules for a particular set of guidelines, select **Import All**.

    <img alt="Import API Governance rule from Postman library" src="https://assets.postman.com/postman-docs/import-postman-rule-from-rule-library-10.12.0.jpg"/>

1. Once you import new rules from the library, add the rules to a workspace group to [turn them on](#turning-configured-rules-on-and-off) for the workspaces in the group.

### Adding custom rules

You can create new custom governance rules for Postman to evaluate your API's definition in OpenAPI format. Postman provides you with a boilerplate rule to help you start writing your custom governance rules. You can use snippets of commonly-used property-value pairs to help you write your custom governance rules.

You can also add an API definition to the editor in OpenAPI format, enabling you to test whether your custom rule catches violations in the API definition.

To add and test a custom rule, do the following:

1. Select the **Rule Library** tab, and then select the **Rules** tab.
1. Select **Create Rule** dropdown menu. You can select **Create New** to create a new rule from scratch. You can also select **Upload File(s)** to upload one or more rule files in valid YAML or JSON format.

    > If you upload two or more rule files using the **Upload File(s)** option, the rules will be combined into a single custom governance rule.

1. Define the custom rule in the editor. It must adhere to [custom rule guidelines](/docs/api-governance/configurable-rules/spectral/). Errors will display at the bottom of the editor if they're found in the custom governance rule.

    You can use a curated list of commonly-used property-value pair snippets to write your rules. Select **<** in the middle pane to show the snippets. Selecting a snippet adds the property-value pair automatically to your rule, helping you get started quickly with writing rules. Once added to your rule, you can edit the snippets to meet your specific requirements.

    > Postman will prompt you with suggestions as you enter text. Select one to autocomplete your rule.

    <!-- -->

    > You can write and add custom functions to your custom governance rules. For more information, see [Adding custom governance functions](/docs/api-governance/configurable-rules/configuring-custom-governance-functions/).

1. Optionally, you can [test whether your custom rule catches violations in an API definition](#testing-custom-rules).

1. Select **Create Rule**. You can find your new rule under **Created by your team**.

    <img alt="Create a custom API Governance rule" src="https://assets.postman.com/postman-docs/v10/api-governance-create-custom-rule-v10-21.jpg"/>

1. Once you add a custom rule, add the rule to a workspace group to [turn it on](#turning-configured-rules-on-and-off) for the workspaces in the group.

> You can't create a custom rule that duplicates an existing rule.

## Turning configured rules on and off

You can turn individual governance rules on or off for various workspaces to meet your team's development needs. You can add governance rules to the default **All workspaces** group, applying governance rules to all workspaces in your team. You can also create a workspace group, and apply governance rules to specific workspaces.

Your team will only see violations in your API's definition for the governance rules explicitly applied to the workspace it resides in.

To add governance rules to all workspaces in your team, do the following:

1. Select the **Workspace Groups** tab.
1. Select the default **All workspaces** workspace group, then select **Add Rules**.
1. Select the checkbox next to governance rules to add them to the workspace group. You can search for governance rules by rule name, and filter them by severity and source.

    <img alt="Turn individual rules on and off" src="https://assets.postman.com/postman-docs/v10/api-governance-turn-rules-on-off-v10-21.jpg"/>

1. Select **Review Changes**.
1. Review your changes, then select **Apply Changes** to confirm. Rules added to the **All workspaces** workspace group will be applied to all workspaces in your team.

To create a workspace group and add governance rules to it, do the following:

1. Select the **Workspace Groups** tab, then select **Create Group**.
1. Enter a name for the workspace group.
1. Select **Add Workspaces** to add workspaces to the workspace group. Select the checkbox next to workspaces to add them to the workspace group.

    To search for workspaces by name, select **Search workspaces**, then enter your search terms. To filter workspaces by [workspace tags](/docs/collaborating-in-postman/using-workspaces/managing-workspaces/#tagging-a-workspace), select the **Filter by tags:** dropdown, then select the checkbox next to each tag you'd like to filter by. If you select more than one tag, the results show workspaces with at least one of the selected tags.

    <img alt="Add workspaces to a workspace group" src="https://assets.postman.com/postman-docs/v10/api-governance-add-workspaces-to-group-v10-21.jpg"/>

1. Select **Add Rules** to add governance rules to the workspace group. Select the checkbox next to governance rules to add them to the workspace group. You can search for governance rules by rule name, and filter them by severity and source.

    <img alt="Turn individual rules on and off" src="https://assets.postman.com/postman-docs/v10/api-governance-turn-rules-on-off-v10-21.jpg"/>

1. Select **Review Changes**.
1. Review your changes, then select **Apply Changes** to confirm. Rules added to the workspace group will be applied to the added workspaces.

To edit the workspaces added to a workspace group, select an existing workspace group, then select **Edit** under **Workspaces**. To add workspaces, select the checkbox next to a workspace. To remove workspaces, clear the checkbox next to a workspace.

To edit the governance rules added to a workspace group, select an existing workspace group, then select **Edit** under **Rules**. To turn a governance rule on, select the checkbox next to the rule name. To turn a governance rule off, clear the checkbox next to the rule name.

## Editing custom rules

You can edit custom governance rules you created earlier. You can also test whether your custom rule catches violations in an API definition in OpenAPI format.

1. Select the **Rule Library** tab, and then select the **Rules** tab.
1. Under **Created by your team**, select the name of the custom rule you'd like to edit.

    <img alt="Create a custom API Governance rule" src="https://assets.postman.com/postman-docs/v10/edit-custom-governance-rule-v10.jpg"/> <!-- TODO: update screenshot -->

1. Edit the custom rule in the editor.
1. Optionally, you can [test whether your custom rule catches violations in an API definition](#testing-custom-rules).
1. Select **Save Changes**.

## Testing custom rules

When you [add a custom rule](#adding-custom-rules) or [edit a custom rule](#editing-custom-rules), you can test whether your custom rule catches violations in an API definition. If you want to enforce a specific rule in your team, you can add an API definition that has violations to test whether your rule catches them. You can also edit an API definition in the editor to trigger rule violations, enabling you to test whether your rule catches the new violations. Your API definition must be in OpenAPI format.

In the custom rule editor, select the test rule icon <img alt="Console icon" src="https://assets.postman.com/postman-docs/icon-console-v9.jpg#icon" width="16px"> in the right pane, then add an API definition in OpenAPI format. You can add an API definition as follows:

* Select **Select API from workspace** to open an API definition from a workspace in your team. Choose an API, then select **Evaluate API**. Any changes to the API definition in the editor won't affect your original API definition.
* Paste raw text or a URL to the API definition file in YAML or JSON format.
* Drag and drop an API definition file, or upload a file in YAML or JSON format.

<img alt="Test a custom rule with an API definition" src="https://assets.postman.com/postman-docs/v10/api-governance-test-custom-rule-v10-21-b.jpg"/>

Syntax errors and rule violations will display at the bottom of the editor if they're found in the API definition.

<img alt="Select an API definition to test a custom rule" src="https://assets.postman.com/postman-docs/v10/api-governance-select-api-definition-v10-21-b.jpg"/>

To test your custom rule with a different API definition, select **Use Another API** in the top right of the editor, then add a new API definition.

## Removing rules from your API Governance configuration

To remove an API Governance rule, locate the rule in your team's rule library and select the delete icon <img alt="Delete icon" src="https://assets.postman.com/postman-docs/icon-delete-v9.jpg#icon" width="12px"> next to its name. You can later choose to [re-import it from the rule library](#importing-rules-from-the-rule-library).

If you remove a custom rule using the delete icon <img alt="Delete icon" src="https://assets.postman.com/postman-docs/icon-delete-v9.jpg#icon" width="12px">, you'll need to add it back into Postman using [**Create Rule**](#adding-custom-rules) if you want to use it again.
