```javascript
/**
 * @file Contact.jsx
 * @description Contact section component for Rahmat's portfolio.
 * @author Rahmat Khan
 * @version 1.0
 *
 * @overview
 * This component renders a contact form with a 3D Earth canvas background.
 * The form is integrated with Supabase to store submissions securely.
 * Features include animations with Framer Motion and responsive design.
 *
 * @prerequisites
 * - Node.js and npm installed.
 * - Supabase project set up with a 'contacts' table.
 * - Environment variables (VITE_SUPABASE_URL, VITE_SUPABASE_ANON_KEY) in a .env file.
 *
 * @installation
 * 1. Install dependencies: `npm install`
 * 2. Set up .env with Supabase credentials (do not commit .env).
 * 3. Run: `npm run dev` to start the development server.
 *
 * @usage
 * - Fill out the form to send a message (data stored in Supabase).
 * - View submissions in the Supabase dashboard.
 *
 * @notes
 * - Ensure .gitignore includes .env to prevent sensitive data leaks.
 * - Test locally before deployment.
 *
 * @lastUpdated August 07, 2025
 */
import React, { useRef, useState } from "react";
import { motion } from "framer-motion";
import { supabase } from "../utils/supabase";
import { styles } from "../styles";
import { EarthCanvas } from "./canvas";
import { SectionWrapper } from "../hoc";
import { slideIn } from "../utils/motion";

