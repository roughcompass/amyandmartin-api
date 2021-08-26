# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
  NotificationMailer.announcement(email: c.email, code: "").deliver_now
failures = []
  
while failures.size > 0
    email = failures.pop
    NotificationMailer.announcement(email: email, code: "").deliver_now
    rescue
        failures.push(email)
end

fa.each do |c|
    if c.email
        NotificationMailer.announcement(email: c.email, code: "").deliver_now
    end
    rescue
        failures.push(c.email)
end