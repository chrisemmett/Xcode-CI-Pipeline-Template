# App Review Information (first submission)

App Store Connect's **App Review Information → Notes** field isn't marked as
required, but a new app submitted without it comes back with *Guideline 2.1 -
Information Needed*. Fill it in before the first (v1.0) submission and keep it
current for later ones.

In this repository the Notes field is `fastlane/metadata/review_information/notes.txt`,
uploaded by `fastlane ios metadata` (`docs/release.md`, "App Store metadata").
It starts as a skeleton of the items below marked `TODO`; the lane's
`--release` check refuses to upload it until every `TODO` is gone. The limit is
4000 characters.

Some items don't fit in the text file:

- **The screen recording** (item 1) is a video. Attach it to your reply to App
  Review in App Store Connect; it doesn't need a link in the notes.
- **Demo account credentials** go in App Store Connect's *Sign-in required*
  fields, not in a committed file. If the app has several account types, say in
  the notes where to get the others rather than committing passwords.
- **Regulatory documents** (item 6) are attachments too.

## What App Review asks for

The rejection text, verbatim, as received for a new app submission:

> **Guideline 2.1 - Information Needed - New App Submission**
>
> We need additional information to better understand the app and complete the review.
>
> Note: Before submitting, run the submitted build through your own testing and quality assurance process on supported physical devices. App Review is intended for apps and metadata that are complete and ready for App Store customers.
>
> If the app is ready for review, follow the directions below.
>
> **Next Steps**
>
> Reply in App Store Connect with all of the following information and also add this information to the Notes field of the App Review Information section in App Store Connect, for reference on future submissions:
>
> 1. A screen recording captured on a physical device, running the latest operating system, demonstrating the app's functionality. The recording must begin with launching the app and show the typical user flow. If the app has any of the following, include them in the recording:
>    - Account registration, login, and account deletion flows. Account deletion is required in apps that support account creation.
>    - Any user-generated content, including the required content reporting and blocking mechanisms.
>    - Accessing paid content or features within the app.
> 2. A description of the app's purpose and target audience, including the problem it solves and the value it provides
> 3. Instructions for setting up and accessing the app's main features, including any required login credentials or sample files
> 4. A list of the external services, tools, or platforms the app uses to deliver its core functionality (for example, data providers, authentication services, payment processors, or AI services)
> 5. Describe any regional differences in the app's features or content, or confirm that the app functions consistently across all regions
> 6. If the app operates in a highly regulated industry or includes protected third-party material, provide any relevant documentation or credentials to demonstrate you are authorized to provide these services or protected material
>
> **Prevent Common Issues**
>
> - Guideline 2.1 - Bugs and crashes: Apps are reviewed on physical devices to mirror real-world conditions. Test the app on each supported device platform before submitting. Use TestFlight to distribute builds for beta testing on real devices.
> - Guideline 2.1 - Accessing the app: If the app includes account-based features, provide up-to-date login credentials for a demo account in App Store Connect. If the app has multiple account types, provide credentials for each type in the Notes field.
> - Guideline 2.3.3 - Screenshots: App screenshots on the App Store must show the actual app in use, and not merely the title art, login page, or splash screen.
> - Guideline 3.1.1 - In-App Purchase: In-App Purchase products should be configured and submitted alongside the app.
> - Guideline 3.2 - Other Business Models: If your app is intended to be used by specific businesses, organizations or employees then use one of the other distribution options available to you through the Apple Developer Program Account.

## Before submitting v1.0

- [ ] Screen recording on a physical device, latest iOS, starting from launch:
      the typical flow, plus sign-up, sign-in and account deletion, reporting and
      blocking of user-generated content, and paid content, where the app has them.
      Attached to the reply to App Review in App Store Connect.
- [ ] `notes.txt` covers items 2 to 6, with no `TODO` left.
- [ ] Demo account credentials in App Store Connect's *Sign-in required* fields
      (one per account type), if the app has accounts.
- [ ] Every In-App Purchase is configured and added to this version's submission.
- [ ] Screenshots show the app in use, not the splash screen, title art or login page.
- [ ] The build has been through TestFlight on every supported device family
      (iPhone and iPad).
- [ ] `fastlane ios metadata` run, and the Notes field checked in App Store Connect.
