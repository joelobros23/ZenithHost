# Project Plan: ZenithHost

**Description:** A simplified web hosting platform designed for ease of use, built on Ruby on Rails with SQLite, Tailwind CSS, and Devise.


## Development Goals

- [ ] Configure tailwindcss-rails by running `./bin/rails tailwindcss:install` and update application.tailwind.css to include base styles and components.
- [ ] Modify the Domain model to include validations: `validates :name, presence: true; validates :plan, presence: true`.
- [ ] Customize the Domains index and form views (app/views/domains/*) using Tailwind CSS classes to enhance the user interface. Focus on responsiveness and readability.
- [ ] In the Domains controller (app/controllers/domains_controller.rb), before actions, implement authentication with `before_action :authenticate_user!`. Override `create` and `update` actions to automatically assign the domain to the current user: `@domain.user = current_user`. Add `user_id` to the permitted parameters in `domain_params`.
- [ ] Add a user dashboard (e.g., a `UsersController`) with a view that displays a personalized welcome message (`Hello, [User's Email]!`) and lists the user's domains. Protect this dashboard with `before_action :authenticate_user!`.
- [ ] Implement domain status management (e.g., 'active', 'pending', 'suspended') and display the status prominently in the domain list.
- [ ] Add basic pricing tiers to the `plan` attribute and display them clearly on the domain creation form.
- [ ] Add a simple home page with a basic landing page design using Tailwind CSS.
- [ ] Ensure all views are accessible and responsive across different screen sizes.
