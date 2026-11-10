# Description of my Work Experience for an Engineering Consultancy:
### This was Work Experience I did for my [T-Level Course](https://qualifications.pearson.com/en/qualifications/t-levels/digital-software-development.html), I used C# as the coding language.
#### I attended one day a week from November 2025 - 10th of November 2026, 30 days in total. ([full list of dates](#dates))

#### Description of the company and my job:

During my work placement for my course I worked at an engineering consultancy that designs the mechanical and electrical systems inside buildings, such as heating, ventilation, air conditioning, lighting and power, and water services. The company works with architects, contractors and clients to plan these systems at the design stage of construction projects. 

The people working there utilised a piece of software called [Revit](https://www.autodesk.com/uk/products/revit/overview) (by AutoDesk).

My job was to create something called "[add-ins](https://revizto.com/resources/blog/revit-addins-addons-plugins)" for Revit, to help the engineers work faster by automating repetitive tasks within an already existing codebase (one of the engineers made add-ins already and I was working with him during my time).

Essentially, an add-in can turn a longer task (requiring multiple clicks / edits) into a much shorter one (making it a couple clicks / more efficient).

| # | Entry |
|:-:|-------|
| 1 | [Initial Work](#start) |
| 2 | [Filter Manager](#filter_man) |


> **Note:** I cannot show my code for these add-ins due to a Non-Disclosure Agreement I signed, however I am allowed to show off pictures of each piece of work I did and explain what they do (I was told I was allowed to do this by the person who owns the codebase for these add-ins).

<details open>
<summary><h2 id="start">Initial Work:</h2></summary>

Since I was just getting into Revit, I started by developing A "Copy Parameters" add-in for Revit. 

**Explanation of what Parameters are:**

Each object in Revit (whether a duct, a light fixture, a pipe, or a room) will have parameters, which are named fields of information. Some of these are part of the software itself, such as Length, Level or System Type. Other data fields include those created by the company, such as Asset Code, Zone, Maintenance Category or Fire Rating. Engineers fill these in so they can appear in schedules, tags and drawings, and be handed over to clients.

Doing this one by one will take a lot of time, so a Copy Parameters add-in would allow for more time efficiency in the office.

**What I learned:**

Working in someone else's codebase was overwhelming at first, especially one built for engineering software I had never used.

However, I did eventually persevere after exploring through the pre-existing code, as well as Revit's API and forums related to Revit.

<p align="center">
  <a href="images/CopyParameters_labelled.png">
    <img src="images/CopyParameters_labelled.png"
         alt="The Copy Parameters add-in window in Revit"
         title="Click to view full size"
         width="500">
  </a>
  <br>
  <em>My first Revit add-in, Copy Parameters (click to enlarge)</em>
</p>

1. **Parameter list**: every parameter on the selected element, each with a tick box to choose which ones to copy.
2. **Select All / Deselect All**: ticks or clears every parameter at once.
3. **Copy Value**: copies the values of the ticked parameters onto the target element(s).
4. **Cancel**: closes the window without changing anything.
</details>

<details open>
<summary><h2 id="filter_man">Filter Manager:</h2></summary>

After I finished my work on "Copy Parameters", I was assigned to created a "Filter Manager".

**Explanation of what a Filter is in Revit:**

A filter solves visual clutter in a bust drawing, this is done by picking out objects that match a set of rules and changing how they look in a view.

Each filter is made of two parts:

- **Rules**: which objects the filter applies to. These are based on categories and parameters, for example "all Ducts where System Type equals Supply Air".
- **Graphic overrides**: what happens to the matching objects in the view. They can be given a different colour, line style or transparency, or be hidden completely.

For example, an engineer could make supply air ducts show in blue and extract air ducts in red, so the two systems can be told apart at a glance on a drawing.

Filters are applied per view, so the same model can look different depending on who the drawing is for. Because the rules are based on parameters, the filters update automatically as the model changes: any new duct set to "Supply Air" will turn blue without anyone needing to colour it by hand.


**Explanation of what the "Filter Manager" would consist of:**

The Filter Manager (originally called the "Filter Generator") is an add-in that lets engineers set up and edit the filters inside Revit's View Templates from one window, instead of going through Revit's own menus filter by filter.

A **View Template** is a saved set of display settings that can be applied to many views at once, so every drawing of the same type looks consistent. Filters are stored inside these templates, which means changing a filter's appearance normally means opening each template and editing every filter by hand.

The Filter Manager works in these steps:

1. **Choose a template**: The user selects the View Template Type and subsequently the specific template to be edited.
2. **Choose a filter**: From the filters contained within the template, the user selects the specific filter (or rule) they wish to edit.
3. **Match it to the company colour list**: The add-in searches for the filter name within an Excel file that contains the list of filter names used across the company, along with their corresponding RGB color values. The relevant color is displayed in a colored box, allowing the user to immediately see which color should be assigned to the filter.
4. **View and edit the filter's settings**: The add-in retrieves the current filter settings from Revit and allows the user to adjust them, including:
   - Foreground pattern and color
   - Background pattern and color
   - Line pattern, color, and weight
   - Transparency
   - Status (enabled/visible) as well as the display of foreground and background patterns
5. **Apply to multiple filters**: the user can select several filters at once and save all of these settings to every one of them in a single action.

1. **Select Template**: The user selects the View Template Type and subsequently the specific template to be edited.
2. **Select Filter**: From the filters contained within the template, the user selects the specific filter (or rule) they wish to edit.
3. **Cross-reference with the company-wide color list**: The add-in searches for the filter name within an Excel file that contains the list of filter names used across the company, along with their corresponding RGB color values. The relevant color is displayed in a colored box, allowing the user to immediately see which color should be assigned to the filter.
4. **View and edit filter settings**: The add-in retrieves the current filter settings from Revit and allows the user to adjust them, including:
   - Foreground pattern and color
   - Background pattern and color
   - Line pattern, color, and weight
   - Transparency
   - Status (enabled/visible) as well as the display of foreground and background patterns
5. **Apply to multiple filters**: The user can select several filters simultaneously and apply settings to all of them in a single step.

By combining information from Revit with data from an Excel file, the "Filter Manager" ensures that filter colors consistently adhere to company standards. Furthermore, it streamlines a time-consuming, repetitive process, reducing it to just a few mouse clicks.

Because it combines information from both Revit and the Excel file, the Filter Manager keeps the filter colours consistent with the company's standards, and it turns a long, repetitive task into a few clicks.


</details>

<details>
<summary><h3 id="dates">Exact Dates:</h3></summary>

- Tuesday 25th November 2025
- Tuesday 2nd December 2025
- Tuesday 9th December 2025
- Tuesday 16th December 2025
- Tuesday 6th January 2026
- Tuesday 13th January 2026
- Tuesday 27th January 2026
- Tuesday 3rd February 2026
- Tuesday 10th February 2026
- Tuesday 24th February 2026
- Tuesday 3rd March 2026
- Tuesday 10th March 2026
- Tuesday 17th March 2026
- Tuesday 24th March 2026
- Tuesday 31st March 2026
- Tuesday 21st April 2026
- Tuesday 28th April 2026
- Tuesday 5th May 2026
- Tuesday 16th June 2026
- Tuesday 23rd June 2026
- Tuesday 30th June 2026
- Tuesday 8th September 2026
- Tuesday 15th September 2026
- Tuesday 22nd September 2026
- Tuesday 29th September 2026
- Tuesday 6th October 2026
- Tuesday 13th October 2026
- Tuesday 20th October 2026
- Tuesday 3rd November 2026
- Tuesday 10th November 2026

</details>
