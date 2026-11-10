# Free Render demo deployment

This configuration uses one free Render web service to serve the React frontend and Flask API. It intentionally has no persistent disk or paid database.

## Deploy
1. Push the contents of this folder to a GitHub repository. `backend/`, `frontend/`, and `render.yaml` must be at the repository root.
2. In Render, choose **New + -> Blueprint** and connect the repository.
3. Review the service. Confirm the plan is **Free** before creating it. If Render shows a paid plan or asks you to add a paid disk, stop and do not approve it.
4. Wait for deployment and open the `onrender.com` URL assigned by Render.
5. Check `https://YOUR-SERVICE.onrender.com/api/health` and then test public registration, complaint submission, police login, and **All Complaints -> View prediction**.

## Demo limitations
- Free service local storage is ephemeral. SQLite accounts and complaints can be lost after a restart, spin-down, or redeploy. Recreate fictional demo accounts/complaints when needed.
- Free services can spin down after inactivity, so the first page load may be slow.
- Use synthetic data only. Do not enter real victim details, phone numbers, bank information, or real complaint records.
- The map shows an illustrative candidate locality, not a live suspect location. The demo confidence score is not a validated probability.
- This prototype is not suitable for real police/citizen case handling without a security review and a properly managed persistent database.
