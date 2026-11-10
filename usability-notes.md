# Usability Notes: Begah Homes v0.1.2

These are not bugs. Everything here works as built, but could be clearer for users. Each note links to the test where it was seen.

## UX-001: Property Code helper text is cut off
- Seen in: Test 2.1 to 2.3, login screen
- Issue: The helper text reads "Tenants & staff only, owners leav..." and the ellipsis hides the end of the instruction.
- Why it matters: Owners may not know what to enter in the Property Code field.
- Suggestion: Shorten the text (for example, "Owners: leave blank") or let it wrap onto two lines.

## UX-002: Logout has no confirmation
- Seen in: Test 2.7, Portfolio screen
- Issue: Tapping the logout icon signs the user out immediately.
- Why it matters: An accidental tap logs the user out with no warning.
- Suggestion: Add an "Are you sure you want to log out?" prompt.

## UX-003: No email format check on the login screen
- Seen in: Test 2.4, login screen
- Issue: Entries like "abc@" and "abc@gmail" are sent to the server and return "Invalid Credentials", with no format message.
- Why it matters: Users who mistype their email get a vague message and may think their password is wrong.
- Suggestion: Check the format before sending. The field also accepts phone numbers, so the check must allow both.
## UX-004: Login details must be retyped after every logout
- Seen in: Test 2.8, login screen
- Issue: After logging out, the Property Code, email and password fields come back empty. There is no "Remember me" option.
- Why it matters: Staff and tenants who log in often must retype all three fields each time.
- Suggestion: Offer a "Remember me" option, or at least prefill the Property Code and email.

## UX-005: No "Forgot password" or "Sign up" link on the login screen
- Seen in: Phase 2 login screen
- Issue: The login screen only has the three fields, Sign In, and "Just browsing? See listings". There is no way to reset a forgotten password or register.
- Why it matters: A user who forgets their password has no way to recover it from the app.
- Suggestion: Add a "Forgot password?" link. If accounts are created by owners or staff only, say so on the screen.