# Bug Report: Signup Redirect Bug for “Work for Membership” Users

## Reported by: Austin Aguguo (@seer_98 on Discord)  
## Date: April 2025

---

## Summary
When trying to sign up using the **“Work for Membership”** option, the site incorrectly redirects to a **paid checkout page powered by Unlock**, instead of processing the free membership flow.

---

## Steps to Reproduce

1. Visit the LexDAO membership signup page. https://lexdao.net/membership/
2. Select **“Work for Membership”** from the options.
3. Submit the form.
4. My initial attempts (from December 2024) showed the error message, **"There waas an error submitting membership application data. Please try again later or contact the website administrator"** 
5. Now (April 2025), instead of confirming the free membership, the site redirects to an Unlock-powered **payment page**.
6. This behaviour happens both on desktop (where it sometimes hangs), and on mobile (where it gets past the loading screen but still asks for payment).

---

## Expected Behavior
- Users selecting “Work for Membership” should not be directed to the payment page.
- The form should correctly process free-tier membership selections and skip the Unlock checkout entirely.

---

## Additional Notes
- The issue appears to stem from a **broken redirect or logic error** in the form handler/backend.
- I also experienced **an infinite loading screen** on desktop when Unlock was invoked, both for the **"Work for Membership"** and **"Individual Membership"** options. This may be a separate issue to follow up with the Unlock Protocol team.
- I tested this across both mobile and desktop to confirm consistency, and it persisted on desktop.

---

## Recommendation
- Investigate and fix the redirect logic for “Work for Membership” in the form backend.
- Ensure form fields map correctly to the intended flow (free vs paid).
- Optionally add debug logs to track tier selection and redirection logic.

---

Happy to answer follow-up questions or test again after fixes.
